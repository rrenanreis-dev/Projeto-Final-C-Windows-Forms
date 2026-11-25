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

![Tela de Cadastro](assets/02-cadastro.png)

### 3. Confirmação de Cadastro
Feedback visual exibindo a mensagem de confirmação após salvar o registro.

![Cadastro Concluído](assets/03-cadastro-sucesso.png)

### 4. Busca e Listagem
Visualização dos bovinos cadastrados na tabela, com campo de busca e ações de **Remover** e **Alterar**.

![Busca e Listagem](assets/04-buscar.png)

### 5. Confirmação de Exclusão
Caixa de diálogo solicitando confirmação antes de remover o registro selecionado.

![Confirmação de Exclusão](assets/05-remover.png)

### 6. Alteração de Registro
Aba dedicada para editar os campos de um bovino selecionado e confirmar a alteração.

![Alterar Bovino](assets/06-alterar.png)
