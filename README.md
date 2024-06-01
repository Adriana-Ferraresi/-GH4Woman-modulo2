# GH4Woman-modulo2
Atividade 2 - Entendendo os repositórios do Github
<hr/>

# Laboratório – Módulo 2: Working with GitHub Repositories

## 2.2 Adicionando Arquivos Através da Linha de Comando

### Requisitos: 

- Um repositório criado no github.com
- Software Git Bash já está instalado

## 2.2.1 Clone de repositório

- Nesta etapa, clonaremos um repositório. A essência da clonagem de repositório é capturar um repositório remoto<br>
 (criado no GitHub.com) e replicá-lo localmente e então teremos um repositório git local igual ao existente remotamente,<br>
 sendo esse repositório sua propriedade ou de outra pessoa.

### Procedimento:

1. Crie uma nova pasta em “Documentos”, essa será nossa pasta do repositório local git.
   - Abra o explorador de arquivos do Windows
   - Clique em “Documentos
   - Crie uma nova pasta  com o nome gh4w (botão direito do mouse, selecione new e depois Folder)
  
2. Acesse a pasta e copie seu endereço.

3. Abra o Git Bash.  

   - Depois da instalação, vá até o menu iniciar e busque por Git Bash
   - Selecione Git Bash na lista de resultados
   
4. Com o terminal aberto, execute o comando a seguir para acessar a pasta criada anteriormente. 
````bash
cd “<endereçoPasta>”
````

5. Acesse github.com no seu navegador e vá até a página do seu repositório

6. Localize o botão “Code” e copie o link HTTPS

 7. Execute o comando:  
````bash
git clone <linkCopiado>
````
### Resultado:

- Temos o clone do repositório do GitHub em um repositório local. A pasta criada no passo 1 agora deve conter uma<br>
  pasta, que é repositório clonado, contendo todos os arquivos do repositório remoto.

## 2.2.2 Adicionando arquivo através de linha de comando  

### Procedimento:

1. Voltar ao terminal e executar o comando:
````bash  
cd <nomeRepositorio>
````
  - Este comando levará ao repositório git local, que é o repositório clonado.O terminal indicará que agora estamos no<br>
    repositório e na branch "main".

2. Como boa prática, não devemos fazer alterações diretamente na branch "main". Execute o seguinte comando para<br>
   criar uma nova branch:
````bash  
git checkout -b <nomeBranchNova>
````
  - Este comando cria a nova branch e já nos coloca nela, ou seja, as alterações feitas nos passos seguintes estarão nesse escopo.

3. Agora execute o comando:
````bash
touch <nomeDoArquivo>
````
  - Esse comando adicionará um arquivo .txt "vazio" ao repositório na branch “BranchExemplo”

4. Em seguida, execute o comando:
````bash
git add .
````
  - Utilizando o comando com  “.” aplicaremos o comando add a todos os arquivos da pasta, para selecionar arquivos específicos<br>
    basta substituir o “.” pelo nome dos arquivos com suas extensões, exemplo: git add arquivo1.txt arquivo2.js

5. Depois, execute o comando:
````bash
git commit -m "<Descrição>"
````
 - Esse comando “comita” a alteração feita no repositório local, no caso, a adição de 1 arquivo através do comando<br>
   com o git add. Perceba que o Git Bash detectará as alterações feitas e apontará que houve um arquivo alterado,<br>
   ou seja, o arquivo criado na pasta.

6. Em seguida, execute o comando:
````bash
git push --set-upstream origin <nomeBranchNova>
````

### Resultado:
 - O resultado até aqui é um pouco diferente da inserção de arquivos através da interface do GitHub, visto que<br>
   não há uma criação automática de um pull request, como já é sinalizado na resposta, que nos orienta a criar<br>
   um pull request diretamente na interface do GitHub.
 - Acesse a página do repositório no navegador. Temos uma indicação através de um banner de que ocorreram<br>
  "pushes" na branch que foi criada no terminal.

### Sugestão:
- Explore desafios mais complexos, como a edição de arquivos, como o README, e o commit desses arquivos<br>
  para suas branches originais ou novas branches.




