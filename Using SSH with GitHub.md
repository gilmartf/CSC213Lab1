# Using SSH with GitHub

More detailed information about this process can be found [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). The information below summarizes this info into the minimum
required steps:

For: 

- Windows:
    - Open Git Bash.
- macOS, Linux: 
    - Open a Terminal.

## 0. Checking for SSH Keys
Enter in the command:
```
ls -al ~/.ssh
```

- If you see files named `id_ed25519` and `id_ed25519.pub` you can go directly to [step 2](#2-adding-a-private-ssh-key-to-the-ssh-agent).
- Otherwise, if you see a message like: `ls: cannot access '~/.ssh': No such file or directory.` then go to [part 1](#1-generating-an-ssh-key-pair)

## 1. Generating an SSH Key Pair
1. Run the command:
```
ssh-keygen -t ed25519 -C "your_email@whatever.com"
```
2. Press `Enter` when prompted to "Enter a file in which to save the key." 
    - This saves the key pair to their default location, which is fine for our purposes.
3. At the next prompt enter in a passphrase of your choice.
    - This is what you will need to enter to utilize the key the first time you login to your machine and use SSH (not every
      time you push something to remote repos like with HTTPS!).

Now, if you [check for SSH keys](#0-Checking-for-SSH-Keys), among other files, you should see two that contain the **private** key `id_ed25519` and the **public**
key `id_ed25519.pub`.

## 2. Adding a Private SSH Key to the `ssh-agent`
1. Start the `ssh-agent` in the background:
```
eval "$(ssh-agent -s)"
```
2. Add your **private** key to the `ssh-agent`:
```
ssh-add ~/.ssh/id_ed25519
```

## 3. Adding a Public SSH Key  to GitHub
1. Copy the contents of `id_ed25519.pub` to the clipboard.
2. Login to your GitHub account.
3. Go to Settings -> SSH and GPG Keys -> New SSH Key.
4. Add a relevant title name to your SSH key and click "Add SSH Key".

## 4. Testing the SSH Connection
Enter:
```
ssh -T git@github.com
```
A message should be returned indicating that you are successfully authenticated, but GitHub does not provide shell access.
