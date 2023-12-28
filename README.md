Ansible.. Vault

ssh

`eval "$(ssh-agent -s)"` and `ssh-add ~/.ssh/id_ed25519`


## Backup

1. first
    ```
    gpg --list-secret-keys --keyid-format LONG
    ```
2. It will show something similar to this.
    ```
    sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10]
    ```
3. Characters after the slash are the ID of the private key. Export the private key.
    ```
    gpg --export-secret-keys $ID > key.asc
    ```


gpg import

`gpg --import key.asc`


do not forgot this `GPG_TTY=$(tty)` in bashrc
