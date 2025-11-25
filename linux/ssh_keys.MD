### SSH Keys for git

C|A
-|-
ssh-keygen -t rsa -b 4096 -m PEM -f ~/.ssh/id_rsa_azure -C "azure" | FOR AZURE
ssh-keygen -f ~/.ssh/id_rsa_github -C "github" | FOR GITHUB 
ssh-keygen -t ed25519 -C "comment" -f ~/.ssh/id_ed25519 | Generate new ED25519 key

#### flag explanations
`-c <comment>` - add comment to the .pub of the key  
`-m PEM` ensures compativility (produces a key starting with ssh-rsa)  
And don't forget to add the keys to the git user
```
cat ~/.ssh/id_rsa_github.pub
cat ~/.ssh/id_rsa_azure.pub
```

## Github + Azure coex config
`~/.ssh/config`:
```
Host azuredevops.company.co.il
  IdentityFile ~/.ssh/id_rsa_azure
  IdentitiesOnly yes
  HostKeyAlgorithms +ssh-rsa
  PubkeyAcceptedAlgorithms +ssh-rsa

Host github.com
  User git
  IdentityFile ~/.ssh/id_rsa_github
```

`IdentityFile` - Force to use a specific identity file (e.g. for support of git + azure)
`IdentitiesOnly yes` - try only this identity file for authentication. And don't try others
`User git` - Should be used for github. Otherwise premission will be denied for a local user name
