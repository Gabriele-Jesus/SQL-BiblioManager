# Banco de Dados ESCOLA - Exercício SQL

Este repositório contém o exercício prático proposto pela escola Pro Talento, para criação de um banco de dados relacional chamado **ESCOLA**. O banco foi projetado com tabelas inter-relacionadas, utilizando chaves primárias e estrangeiras para garantir a integridade dos dados e representar os relacionamentos entre as entidades de alunos, livros e empréstimos.

## Descrição do Exercício

O objetivo deste exercício é criar um banco de dados com as seguintes etapas:

1. **Criar o banco de dados ESCOLA.**
2. **Criar as tabelas:**
   - Tabela **ALUNO** com dados sobre os alunos, incluindo atributos como nome, matrícula, e-mail e endereço.
   - Tabela **LIVRO** para armazenar informações sobre livros disponíveis para empréstimo, incluindo título, autor e a sessão à qual o livro pertence.
   - Tabela **SESSAO** para representar as sessões de livros.
   - Tabela **EMPRESTIMO** que armazena informações sobre os empréstimos feitos pelos alunos.
   - Tabela **LIVRO_EMPRESTIMO**, que representa a relação entre os livros e os empréstimos, permitindo que um livro seja emprestado mais de uma vez.

## Estrutura do Banco de Dados

### Tabelas Criadas:

1. **ALUNO**
   - ID: Identificador único (chave primária)
   - NOME: Nome do aluno
   - MATRICULA: Matrícula única do aluno
   - EMAIL: E-mail do aluno
   - ENDERECO: Endereço do aluno
   - TELEFONE: Telefone do aluno

2. **LIVRO**
   - COD_LIVRO: Identificador único do livro (chave primária)
   - TITULO: Título do livro
   - AUTOR: Autor do livro
   - COD_SESSAO: Código da sessão a que o livro pertence (chave estrangeira)

3. **SESSAO**
   - CODIGO: Identificador único da sessão (chave primária)
   - DESCRICAO: Descrição da sessão
   - LOCALIZACAO: Localização da sessão

4. **EMPRESTIMO**
   - CODIGO: Identificador único do empréstimo (chave primária)
   - DATA_HORA: Data e hora do empréstimo
   - MATRIC_ALUNO: Matrícula do aluno (chave estrangeira)
   - DATA_DEVOLUCAO: Data de devolução do livro

5. **LIVRO_EMPRESTIMO**
   - COD_LIVRO: Código do livro (chave estrangeira)
   - COD_EMPRESTIMO: Código do empréstimo (chave estrangeira)

### Relacionamentos:

- **ALUNO** tem um relacionamento 1:N com **EMPRESTIMO**, onde um aluno pode realizar vários empréstimos.
- **LIVRO** tem um relacionamento N:1 com **SESSAO**, onde vários livros podem pertencer à mesma sessão.
- **LIVRO_EMPRESTIMO** estabelece uma relação N:N entre **LIVRO** e **EMPRESTIMO**, permitindo que um livro seja emprestado mais de uma vez e em diferentes empréstimos.

## Como Usar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/Gabriele-Jesus/<nome-do-repositorio>.git
