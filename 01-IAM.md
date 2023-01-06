# IAM 
### *IAM - CLI - SDK - Cloud Shell*
---
## IAM - Identity and Access Management

- É um serviço da Web que ajuda você a controlar o acesso aos recursos da AWS de forma segura. Você usa o IAM para controlar quem é autenticado (fez login) e autorizado (tem permissões) a usar os recursos.

- Sessão da plataforma aonde você pode criar/cadastrar: Usuarios, Grupos, Permissões, Privilégios, Acessos, Regras e etc... .

- Acesso compartilhado à sua conta da AWS.

- Permissões granulares.

- Acesso seguro a recursos da AWS para aplicações executadas no Amazon EC2.

- Autenticação multifator (MFA).

- Federação de identidades.

- Informações de identidade para garantia.

- Compatibilidade com PCI DSS.

- **Multifactor Authentication** - Pode se logar a plataforma através de: user / password / token / auth ( google authenticator ).

- **Identity Federation** - Pode se logar a plataforma através de: Active Directory (AD) / Facebook / Linkedin / Twitter.

- **Permissions** - Consegue dar permissões do tipo: um usuário consegue criar uma EC2 apenas do tamanho *small*, *12G ram* e *1T de disco*.

- **PCI DSS** - Meios de pagamentos via cartão de uma maneira mais segura.

- **Regras de Acesso** - *Ex.:* Para uma máquina (EC2) acessar um banco de dados (Maria DB), é necessário criar uma *Role (regra)* para que seja possível este acesso.

- **Polices** - Significa o que o algo deve/pode fazer. *Ex.:* Uma maquina EC2 pode ler o DB1 e pode ler e escrever no DB2. *Polices* podem ser aplicadas para *Roles*, *Groups* e *Users*.

- Criando um Usuário:
    - Primeiro adicionamos o nome: angelo.zero
    - Depois selecionamos o tipo de acesso
        - Programmatic access: Habilita um ID de chave de acesso e uma chave de acesso secreta para API, CLI, SDK e outras ferramentas de desenvolvimento da AWS.
        - AWS Management Console access: Habilita uma senha que permite aos usuários fazer login no Console de gerenciamento da AWS ( acesso a AWS na Web ).

- Criando um Grupo: ( *Groups* )
    - Dar um nome para o Grupo
    - Estabelecer as Politicas de acesso (*Policys*)
    - Grupos contém apenas usuários.

- Criando política de senha ( *Policies* )
    - Políticas de acesso é um arquivo JSON
    - Selecionar:
        - Número de caracteres
        - Letras maiúsculas e minúsculas
        - Pelo menos um número
        - Caracter alfanumérico
        - Expira ? Sim ou não
        - Permite usuário alterar a própria senha
        - Não permite reutilzar a mesma senha

- Funções ( *Roles* )
    - Regras para comunicação / acesso entre serviços / grupos / usuários da AWS.

- Chave de Acesso ( *Access Key* )
    - Chaves de acesso para CLI e SDK.

- Grupos contém apenas grupos.

- Sempre aplicar o principio de menos permissões possível.

-  Grupos recebem uma politica ( Policys ) de acesso, um único usuário recebe um política chamada *inline*.

- Uma estrutura de Politica recebe
    - Version
    - Id
    - Statment
        - Sid
        - Effect
        - Principal
        - Action
        - Resource

- Nunca compartilhe sua *access key*!

- Para ver o histórico de acesso de um usuário é necessário ir até o usuário cadasrado e clicar em Consultor de Acesso (*Access Advisor*).

- Nunca use sua conta raiz ( *root* ) exceto para configuração de outras contas AWS

- Para uso de CLI e SDK você precisa gerar uma Access Key.

---

## CLI - Command Line Interface

- Uma ferramente que te permite usar os serviços da AWS usando comando linhas de comando em um prompt 

- Acesso direto a API's publicas

- Você pode desenvolver scripts para gerênciar seus recursos

---

## SDK - Software Development Kit

- Linguagens específicas de API's.

- Habilita seu acesso e gerênciamento dos serviços da AWS programaticamente.

- Incorpora seu aplicativo

- Suporta as linguagens: JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++

---

## Cloud Shell - A terminal in AWS web

- A mesma coisa que o AWS CLI, usa um prompt para executar comando AWS.

---

## Extra
- What is a proper definition of an IAM Role?
    - An IAM entity that defines a set of permissions for making requests to AWS services, and will be used by an AWS service.

- Which of the following is an IAM Security Tool?
    - IAM Credentials report lists all your AWS Account's IAM Users and the status of their various credentials.

- IAM Users access AWS services using their own credentials (username & password or Access Keys).

- Which of the following is an IAM best practice?
    - Don't use the root user account. Use the root account only to create your first IAM User and a few account/service management tasks. For everyday tasks, use an IAM User.

- What are IAM Policies?
    - JSON documents that define a set of permissions for making requests to AWS services, and can be used by IAM Users, User Groups, and IAM Roles

- Which principle should you apply regarding IAM Permissions?
    - Grant least privilege. Don't give more permissions than the user needs.

- What should you do to increase your root account security?
    - Enable Multi-Factor Authentication (MFA). When you enable MFA, this adds another layer of security. Even if your password is stolen, lost, or hacked your account is not compromised.

- Can IAM User Groups contain IAM Users and other User Groups?
    - False, IAM User Groups can contain only IAM Users.

- An IAM policy consists of one or more statements. A statement in an IAM Policy consists of the following, EXCEPT...
    - Version, A statement in an IAM Policy consists of Sid, Effect, Principal, Action, Resource, and Condition. Version is part of the IAM Policy itself, not the statement.

- According to the AWS Shared Responsibility Model, which of the following is AWS responsibility?
    - AWS Infrasstructure