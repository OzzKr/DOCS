# Install GIT (debian/ubuntu) bash apt

## References
>
>Git book online [Git - Book](https://git-scm.com/book/en/v2)

Download git linux
> [Download for Linux and Unix](https://git-scm.com/download/linux)

Verificar posible version instalada

```bash
 git --version
```

update & upgrade distro packages

```bash
sudo apt-get update && sudo apt-get upgrade
```

Install git

```bash
 sudo apt install git
```

For the **latest stable version**

 For Ubuntu, this PPA provides the latest stable upstream Git version

```bash
add-apt-repository ppa:git-core/ppa

apt update

apt install git
```

connect to gitHub using ssh

> <https://docs.github.com/es/authentication/connecting-to-github-with-ssh>

Crear llave ssh

```bash
ssh-keygen -t ed25519 -C "_github_ _username_"
```

Iniciar el agente ssh en segundo plano

```bash
eval "$(ssh-agent -s)"
```

Add your SSH private key to the ssh-agent

```bash
ssh-add ~/.ssh/id_ed25519
```

**_Add the SSH key to your account on GitHub._**

Copy the SSH public key ‘content’ to your clipboard and Paste in github ssh keys

```bash
cat ~/.ssh/id_ed25519.pub
```

Testing your SSH connection

```bash
ssh -T [git@github.com](mailto:git@github.com)

#Result

#Hi _username_! You've successfully authenticated, but GitHub does not provide shell access
```

Create a new repository on the command line

* Create a repository _RepoName_ in GitHub

* Create project folder, add file, and commit

```bash
mkdir helloworld

cd helloworld

echo "# helloworldrepo" >> README.md

git init

git add README.md
```

Realizar commit, se debe tener username configurado

```bash
git commit -m "first commit"
```

If asks, Set username and email

```bash
git config --global user.name "githubUsername"
git config --global user.email githubUsername@users.noreply.github.com
```

Editar el archivo de configuración global con Nano

```bash
git config --edit --global
```

Primer commit local con usuario configurado

```bash
git commit -m "first commit"
```

Renombra rama local a “main”

```bash
git branch -M main
```

Add remote repository to local

```bash
git remote add origin git@github.com:GitUserName/RepoName.git
```

Subir los cambios del local al repositorio remoto

```bash
git push -u origin main
```

## …or push an existing repository from the command line

```bash
git remote add origin git@github.com:GitUserName/RepoName.git

git branch -M main

git push -u origin main
```
