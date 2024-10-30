# integracao-continua-t6

Repositório da disciplina Integração Contínua (Turma 6)

<details>

<summary>
    <h2>Atualizando seu repositório local</h2>
</summary>

O código produzido em sala de aula, e compartilhado neste repositório, pode ser atualizado em seu repositório local com o comando:

```console
git pull
```

No entanto, se você fez alterações no seu repositório local, o comando acima pode gerar conflitos. Para evitar lidar com isso, você pode forçar uma atualização com o repositório remoto por meio dos comandos:

```console
git fetch origin
git reset --hard origin/main
```

O primeiro comando recebe as atualizações mais recentes do repositório remoto, e o segundo descarta todas as alterações locais e atualiza com o histórico mais recente do repositório remoto (branch main).

</details>

<details open>

<summary>
    <h2>Como inciar a aplicação</h2>
</summary>

<h3>Back-end</h3>

A aplicação back-end pode ser iniciada pelo Spring Boot Dashboard ou com o Maven.

1. No Spring Boot Dashboard, clicar em "Run" na aplicação "sgcmapi".

2. Se optar pelo Maven, no prompt de comandos, a partir do diretório `./sgcmapi`:

    a. Para iniciar a aplicação com o Maven:

    ```console
    mvn spring-boot:run
    ```

    Ou

    b. Para compilar o pacote e depois executar o JAR gerado:

    ```console
    mvn package
    java -jar target\sgcmapi.jar
    ```

A aplicação vai iniciar no endereço <http://localhost:9000/>, com acesso local a base de dados MySQL, por meio da porta padrão 3306, além de usuário e senha "root".

<h3>Front-end</h3>

As dependências do projeto não são compartilhadas no repositório. Para instalar as dependências, a partir do diretório `./sgcmapp`, no prompt de comandos, digite:

```console
npm install
```

Para iniciar a aplicação, a partir do diretório `./sgcmapp`, execute o comando:

```console
ng serve
```

A aplicação vai iniciar no endereço <http://localhost:4200>.

</details>

<details open>

<summary>
    <h2>Sites de referência</h2>
</summary>

- Software Delivery Guide (Martin Fowler): <https://martinfowler.com/delivery.html>
- GitHub Docs - GitHub Actions: <https://docs.github.com/pt/actions>
- Docker Docs: <https://docs.docker.com/get-started/overview/>

</details>

<details open>

<summary>
    <h2>Ferramentas</h2>
</summary>

- **Render**
  - Plataforma que será utilizada para deploy com Docker.
  - Criar uma conta: <https://render.com/>
  - [Tutorial de configuração do Render para deploy](https://github.com/webacademyufac/tutoriais/blob/main/render/render.md)
- **Aiven**
  - Serviço de hospedagem de banco de dados MySQL.
  - Criar uma conta: <https://aiven.io/>
  - [Tutorial de configuração do Aiven para hospedagem do banco de dados](https://github.com/webacademyufac/tutoriais/blob/main/aiven/aiven.md)

</details>

<details>

<summary>
    <h3>Outras ferramentas</h3>
</summary>

- **Visual Studio Code**
  - <https://code.visualstudio.com/Download>
- **Extension Pack for Java (Extensão do VS Code)**
  - <https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack>
- **Spring Boot Extension Pack (Extensão do VS Code)**
  - <https://marketplace.visualstudio.com/items?itemName=pivotal.vscode-boot-dev-pack>
- **XML (Extensão do VS Code)**
  - <https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml>
- **Angular Language Service (Extensão do VS Code)**
  - <https://marketplace.visualstudio.com/items?itemName=Angular.ng-template>
- **Git**
  - <https://git-scm.com/downloads>
- **Postman**
  - <https://www.postman.com/downloads/>
- **JDK 17**
  - Para verificar se o JDK está corretamente instalado e configurado, digite no prompt de comandos:

    ```console
    javac -version
    ```

  - Se necessário, realizar a instalação e configuração:
    - Link para download: <https://download.oracle.com/java/17/archive/jdk-17.0.10_windows-x64_bin.msi>
    - Criar a variável de ambiente JAVA_HOME configurada para o diretório de instalação do JDK. Exemplo: “C:\Program Files\Java\jdk-17”.
    - Adicionar “%JAVA_HOME%\bin” na variável de ambiente PATH.
    - Tutorial de configuração: <https://mkyong.com/java/how-to-set-java_home-on-windows-10/>
- **Maven**
  - Para verificar se o Maven está corretamente instalado e configurado, digite no prompt de comandos:

    ```console
    mvn -version
    ```

  - Se necessário, realizar a instalação e configuração:
    - Link para download: <https://dlcdn.apache.org/maven/maven-3/3.8.8/binaries/apache-maven-3.8.8-bin.zip>
    - Adicionar o diretório de instalação do Maven na variável de ambiente PATH. Exemplo: “C:\apache-maven\bin”.
    - Tutorial de instalação: <https://mkyong.com/maven/how-to-install-maven-in-windows/>
- **MySQL**
  - Verificar se o MySQL está funcionando:
    - Para tentar conectar no MySQL, no prompt de comandos digite:

      ```console
      mysql -u root -p
      ```

    - Tentar acessar com senha em branco ou senha igual ao nome de usuário (root).
    - Tutorial para resetar a senha de root, caso necessário: <https://dev.mysql.com/doc/mysql-windows-excerpt/8.0/en/resetting-permissions-windows.html>
  - Remova o banco de dados ```sgcm```, se existir:
    - No prompt de comandos digite:
  
      ```console
      mysql -u root -p
      ```
  
    - Ao conectar no MySQL, execute a seguinte instrução SQL:

      ```sql
      DROP DATABASE sgcm;
      ```
  
  - Se necessário, realizar a instalação:
    - Link para download: <https://dev.mysql.com/downloads/file/?id=516927>
    - [Tutorial de instalação](https://github.com/webacademyufac/tutoriais/blob/main/mysql/mysql.md)
- **Node.js (e npm)**
  - Versão 20 (LTS).
  - Para verificar a versão do Node.js, no prompt de comandos digite:

    ```console
    node --version
    ```

  - Link para download: <https://nodejs.org/dist/v20.14.0/node-v20.14.0-x64.msi>
- **Angular CLI**
  - Versão 17.
  - Para verificar a versão do Angular CLI, no prompt de comandos digite:

    ```console
    ng version
    ```

  - Tutorial de instalação: <https://v17.angular.io/guide/setup-local>
  - Para instalar o Angular CLI, no prompt de comandos digite:

    ```console
    npm i -g @angular/cli@17.3.10
    ```

</details>

<details>

<summary>
    <h2>SGCM - Sistema de Gerenciamento de Clínica Médica</h2>
</summary>

A demonstração de uso das ferramentas e tecnologias abordadas na capacitação é baseada em um projeto de exemplo, o SGCM. A documentação básica deste projeto está disponível [em outro repositório](https://github.com/webacademyufac/sgcmdocs) e aborda os seguintes tópicos:

- [Principais funcionalidades](https://github.com/webacademyufac/sgcmdocs#principais-funcionalides)
- [Histórias de usuário](https://github.com/webacademyufac/sgcmdocs#histórias-de-usuário)
- [Diagrama de Classes](https://github.com/webacademyufac/sgcmdocs#diagrama-de-classes)
- [Diagrama Entidade Relacionamento](https://github.com/webacademyufac/sgcmdocs#diagrama-entidade-relacionamento)

</details>

## Atividades práticas

1. [DUPLA] Criar workflows para integração e implantação contínua para o projeto front-end utilizando o GitHub Actions.

    - Comando para executar os testes: `ng test --browsers=ChromeHeadless --no-watch`
    - Comando para compilar o projeto: `ng build`
    - A implantação pode ser feita em qualquer plataforma. Exemplos:
      - Render (com Docker, a exemplo do que foi feito para aplicação back-end)
        - Dockerfile já está disponível no diretório do projeto front-end.
      - Netlify (não tem suporte para Docker): <https://www.netlify.com/>
      - Vercel (não tem suporte para Docker): <https://vercel.com/>
    - Antes do _**job**_ de _**deploy**_, deve ser executado o workflow de integração contínua do front-end.
    - O _**job**_ de _**deploy**_ deve ser executado apenas se o _**job**_ do CI do front-end for executado com sucesso.
    - **ATENÇÃO**:
      - Para executar os comandos `ng test` e `ng build` no GitHub Actions, é necessário configurar o Node.js e o Angular CLI no ambiente de execução, além de instalar as dependências do projeto.
      - Configurar a constante `API_URL` no arquivo `environment.ts` do projeto front-end.
      - Modificar as configurações de CORS no back-end para adicionar o host da aplicação front-end em produção.
      - A implantação deve ser feita obrigatoriamente por meio do GitHub Actions.

    - Link da atividade: <https://classroom.github.com/a/jHeWW-3U>
    - Entrega: 01/11/2024 - 23:59
