# IAM

## IAM - Identity and Access Management - PT-Br

- É um serviço da Web que ajuda você a controlar o acesso aos recursos da AWS de forma segura. Você usa o IAM para controlar quem é autenticado (fez login) e autorizado (tem permissões) a usar os recursos.

- Sessão da plataforma aonde você pode criar/cadastrar: Usuarios, Grupos, Permissões, Privilégios, Acessos, Regras e etc... .

- **Multifactor Authentication** - Pode se logar a plataforma através de: user / password / token / auth ( google authenticator ).

- **Identity Federation** - Pode se logar a plataforma através de: Active Directory (AD) / Facebook / Linkedin / Twitter.

- **Permissions** - Consegue dar permissões do tipo: um usuário consegue criar uma EC2 apenas do tamanho *small*, *12G ram* e *1T de disco*.

- **PCI DSS** - Meios de pagamentos via cartão de uma maneira mais segura.

- **Regras de Acesso** - *Ex.:* Para uma máquina (EC2) acessar um banco de dados (Maria DB), é necessário criar uma *Role (regra)* para que seja possível este acesso.

- **Polices** - Significa o que o algo deve/pode fazer. **Ex.:** Uma maquina EC2 pode ler o DB1 e pode ler e escrever no DB2. *Polices* podem ser aplicadas para **Roles**, **Groups** e **Users**.

- Criando um Usuário:
    - Primeiro adicionamos o nome: angelo.zero
    - Depois selecionamos o tipo de acesso
        - Programmatic access: Habilita um ID de chave de acesso e uma chave de acesso secreta para API, CLI, SDK e outras ferramentas de desenvolvimento da AWS.
        - AWS Management Console access: Habilita uma senha que permite aos usuários fazer login no Console de gerenciamento da AWS ( acesso a AWS na Web ).

- Criando um Grupo:
    - Dar um nome para o Grupo
    - Estabelecer as Politicas de acesso (**Policys**)

- Criando política de senha
    - Selecionar:
        - Número de caracteres
        - Letras maiúsculas e minúsculas
        - Pelo menos um número
        - Caracter alfanumérico
        - Expira ? Sim ou não
        - Permite usuário alterar a própria senha
        - Não permite reutilzar a mesma senha

---

## IAM - Identity and Access Management - EN-Us