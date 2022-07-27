## Setting Up SSH Keys for GitHub

```
 ssh-keygen -t ed25519 -C example@gmail.com
 eval "$(ssh-agent -s)"
 touch ~/.ssh/config
 cat id_ed25519.pub
 ssh -T git@github.com
 ```

inside `~/.ssh/config`:

 ```
 Host *
  AddKeysToAgent yes
  IdentityFile ~/.ssh/id_ed25519
```