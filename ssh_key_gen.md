# Add key to ssh_key_agent: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key-for-a-hardware-security-key

1. Open Terminal.
2. Replacing the email address in the example with the email address associated with your account on GitHub.

```
ssh-keygen -t ed25519-sk -C "your_email@example.com"
```
Note: If the command fails and you receive the error invalid format or feature not supported, you may be using a hardware security key that does not support the Ed25519 algorithm. Enter the following command instead.
```
 ssh-keygen -t ecdsa-sk -C "your_email@example.com"
```

3. When you are prompted, touch the button on your hardware security key.

4. When you are prompted to "Enter a file in which to save the key," press Enter to accept the default file location.
```
> Enter a file in which to save the key (/home/YOU/.ssh/id_ed25519_sk):[Press enter]
```
5. When you are prompted to type a passphrase, press Enter.
```
> Enter passphrase (empty for no passphrase): [Type a passphrase] : [Press enter]
> Enter same passphrase again: [Type passphrase again] : [Press enter]
```

# Adding a new SSH key to your account: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account

1. Copy the SSH public key to your clipboard.

If your SSH public key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.
```
$ cat ~/.ssh/id_ed25519.pub
# Then select and copy the contents of the id_ed25519.pub file
# displayed in the terminal to your clipboard
```
Tip: Alternatively, you can locate the hidden .ssh folder, open the file in your favorite text editor, and copy it to your clipboard.

2. In the upper-right corner of any page on GitHub, click your profile photo, then click  Settings.

3. In the "Access" section of the sidebar, click  SSH and GPG keys.

4. Click New SSH key or Add SSH key.

5. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal laptop, you might call this key "Personal laptop".

6. Select the type of key, either authentication or signing. For more information about commit signing, see "About commit signature verification."

7. In the "Key" field, paste your public key.

8. Click Add SSH key.

9. If prompted, confirm access to your account on GitHub.
