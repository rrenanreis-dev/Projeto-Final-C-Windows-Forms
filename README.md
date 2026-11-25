# Leilão de Bovinos

Aplicação desktop desenvolvida em **C# (Windows Forms)** integrada ao **MySQL** para gerenciamento e cadastro de bovinos voltados a leilões.

---

## Sobre a Aplicação e Objetivos

O sistema permite centralizar o controle dos animais cadastrados para leilão, oferecendo uma interface simples para as operações do dia a dia:

* **Autenticação:** Tela de acesso inicial (`FormLogin`) para controle de entrada no sistema.
* **Cadastro de bovinos:** Registro de animais com informações de nome, raça, sexo, idade e preço, além de suporte para adicionar novas raças diretamente pela interface.
* **Consulta e filtragem:** Listagem dos animais cadastrados em grade (`DataGridView`) com busca por nome.
* **Alteração e exclusão:** Edição de dados de animais existentes e remoção com confirmação antes de excluir.
* **Persistência e integridade:** Integração com banco de dados relacional (`banco_leilao`) utilizando chaves estrangeiras e *stored procedures* no MySQL.

---

## Tecnologias Utilizadas

* **Linguagem / Interface:** C# (.NET / Windows Forms)
* **Banco de Dados:** MySQL (com *Stored Procedures*)
* **IDE / Ferramentas:** Visual Studio / MySQL Workbench

---

## Instalação e Execução

1. **Clone ou baixe o repositório** para a sua máquina local.
2. **Configure o banco de dados MySQL:**
   * Inicie o servidor MySQL e abra o **MySQL Workbench**.
   * Crie/execute os scripts do banco `banco_leilao` (tabelas relacionadas, chaves estrangeiras e *stored procedures* de cadastro, consulta, alteração e exclusão).
3. **Ajuste a string de conexão:**
   * Abra o projeto no **Visual Studio** e verifique na classe de conexão (ex.: `ConectaBanco.cs`) os parâmetros de servidor, porta, usuário, senha e nome do banco (`banco_leilao`).
4. **Compile e execute:**
   * Restaure/verifique as referências do conector MySQL no projeto e rode a aplicação (`F5` / *Iniciar*).

---

## Demonstração em Telas

### 1. Tela de Login (`FormLogin`)
Acesso inicial ao sistema com usuário e senha.

<img width="822" height="499" alt="login" src="https://github.com/user-attachments/assets/44397356-4f11-481c-93b2-65525cebd6f0" />


### 2. Cadastro de Bovino
Preenchimento dos dados do animal (nome, raça, sexo, idade e preço) e atalho (`+`) para cadastrar raça.

<img width="840" height="450" alt="cadastrar" src="https://github.com/user-attachments/assets/82aaccd8-c3d6-4aa6-8be2-e5ad30160599" />


### 3. Confirmação de Cadastro
<img width="846" height="444" alt="cadastrado" src="https://github.com/user-attachments/assets/dccac40f-7e57-42e9-9e9e-5b998b8041e5" />



### 4. Busca e Listagem
Visualização dos bovinos cadastrados na tabela, com campo de busca e ações de **Remover** e **Alterar**.

<img width="834" height="442" alt="bovinoscadastrados" src="https://github.com/user-attachments/assets/e825d8ff-ca1f-419c-aebb-55dae2104210" />


### 5. Confirmação de Exclusão
Caixa de diálogo solicitando confirmação antes de remover o registro selecionado.

<img width="847" height="447" alt="remover" src="https://github.com/user-attachments/assets/dbcc1f82-b4d0-46fa-8ea3-dd6434685af9" />

### 6. Validação na Aba Alterar
Aviso exibido caso o usuário tente alterar um registro sem antes selecioná-lo na aba **Buscar**.

<img width="838" height="447" alt="erroalterar" src="https://github.com/user-attachments/assets/f7e0ba06-c0ab-4d04-a5f8-797625729d36" />

### 7. Alteração de Registro
Aba dedicada para editar os campos de um bovino selecionado e confirmar a alteração.

<img width="837" height="442" alt="alterar" src="https://github.com/user-attachments/assets/39870437-a4cc-4685-9221-35e02e68ae8f" />

