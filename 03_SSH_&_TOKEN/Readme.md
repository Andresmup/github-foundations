# SSH AND TOKENS

To keep your account secure, you must authenticate before you can access certain resources on GitHub. When you authenticate to GitHub, you supply or confirm credentials that are unique to you to prove that you are exactly who you declare to be.

## SSH
It's a combination of public and private key to authorize remote acces to servers.
A copy of the public and private key reside on the local computer. While a copy of the public key is stored in Github.
Github checks if both publics keys are the same, send an encrypted message, which is de-encrypted locally using the private key. Finally a message is send back, after verify the connection is done.

Steps to create a SSH key locally run in the terminal.
```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
```
Access the public key to copy with.
```sh
cat /your_directory/.ssh/ed25519.pub
```
Paste the public key by adding a new ssh key in Github.
> Settings -> SSH and GPG keys -> Add SSH key

For test the new connection run in the terminal.
```sh
ssh -T git@github.com
```

## DEPLOY KEY
You can launch projects from a repository on GitHub.com to your server by using a deploy key, which is an SSH key that grants access to a single repository.
GitHub attaches the public part of the key directly to your repository instead of a personal account, and the private part of the key remains on your server.

Common use-case of deploy keys are:
 - Build servers or CI/CD third party services that need to clone the repo so they can perform a build or deploy.
 - Single repo access to have a single pair key for a single repo.
 - Avoid using Personal Access Token.

The steps for creating the SSH key are the same but the public key is stored repository Deploy Key.

Paste the public key by adding a new ssh key into the Github repository.
> Repository -> Settings -> Deploy keys -> Add deploy key

> [!NOTE]  
> Select Allow write access if you want this key to have write access to the repository.
>
> A deploy key with write access lets a deployment push to the repository.

## PERSONAL ACCESS TOKEN (PAT)
Personal access token are an alternative to using passwords for authentication to Github when using GITHUB API, the SDK or the CLI.

> [!TIP]  
> Github no longer yet use passwords when interacting with the API, so use PAT instead.

The are 2 types of personal access token.

### Fine Grained Personal Access Token
 - Granted specific permissions.
 - Must have and expiry date.
 - Can only access resources owned by a single user or organization.
 - The repository access can be public repositories (read-only), all repositories
This applies to all current and future repositories owned by the resource owner and select repositories.

To generate it go to:
>Settings -> Developer settings -> Personal Access Tokens -> Fine Grained Token -> Generate New Token

Define a token name, expiration date, resource owner, repository access, permissions and copy the Token valus.



### Classic Token
 - Less secure.
 - Legacy system may be still use clasic tokens.

> [!IMPORTANT]  
> Not recommended for use, avoid using clasic token in new developments.

### Use the Personal Access Token
To check if there is any PAT already (locally or in codespaces) run.
```sh
gh auth token
```

To set a new token with especific permisions and expire date (previously created) follow.
```sh
export GH_TOKEN="your_token" #Paste here the PAT copied before.
env | grep GH #Should return the token generated value.
gh auth token #Now must be change and return the token generated value.
```

