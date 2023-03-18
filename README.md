## Passos Iniciais
### [Configurar chave ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key-for-a-hardware-security-key)
### [Criar um repositório remoto(github)](https://docs.github.com/pt/get-started/quickstart/create-a-repo)
### Criar um repositório local
- mkdir repositoryname
- cd repositoryname
- git init
- vim README.md
- git add .
- git commit -m "initial commit"
### Linkar repositórios utilizando ssh(mais seguro)
- git remote add origin git@github.com:username/repositoryname.git
### Alterar branch de master para main(novo padrão do github)
- git branch -M main
### Enviar repositório local para um lugar da nuvem
- git push -u origin main
### Puxar(pull) atualizações do repositório remoto para o repositório local
- git pull
### Criar uma noca branch
- git checkout -b new_brach
### Listar branchs
- git branch
### Trocar de branch
- git checkout branch_name
### Deletar branch local
Obs: os comandos abaixo devem ser executados em outra branch
- git branch -d branch_name (excluirá a ramificação somente se ela já tiver sido enviada e mesclada com a ramificação remota)
- git brach -D branch_name (forcará a exclusão)
### Deletar branch remota
- git push origin --delete branch_name

## Projetos com Vite
### Subir projeto para o GitHub Pages
- adicione base:"/repository_name/" ao arquivo vite.config.ts
- npm install gh-pages --save-dev
- faça as seguintes configurações no arquivo package.json {... "homepage": "https://user_name.github.io/repository_name/", ... "scripts": {
... "build": "vite build", "predeploy": "npm run build", "deploy": "gh-pages -d dist", ...} ...}
- npm run redeploy
- npm run deploy
