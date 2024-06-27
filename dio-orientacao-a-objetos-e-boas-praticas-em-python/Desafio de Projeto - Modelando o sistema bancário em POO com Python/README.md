# Desafio de Projeto - Modelando o Sistema Bancário em POO com Python

## Objetivo

Iniciar a modelagem do sistema bancário otimizado no [Desafio de Projeto 002](https://github.com/rodolfoom1982/treinamentos/tree/main/dio-dominando-python-e-suas-estruturas-de-dados/Desafio%20de%20Projeto%20002%20-%20Otimizando%20o%20sistema%20banc%C3%A1rio%20com%20fun%C3%A7%C3%B5es%20Python), utilizando POO (Programação Orientada a Objetos)

<br>

## Requisitos

1) Adicionar classes para ***cliente*** e para as operações bancárias ***depositar*** e ***sacar***;
2) Atualizar a implementação do sistema para armazenar os dados de clientes e contas bancárias em objetos e não mais em dicionários;
3) O código deverá respeitar o seguinte diagrama UML:
        >![alt text](readmeFiles/diagramaUML.PNG)

4) ***Desafio Extra***: ao concluir a modelagem das classes e a criação dos métodos, atualizar os métodos que tratam da as opções do ***menu***, de modo que funcionem com as classes modeladas

<br>

## Resolução

> [!NOTE]
> Antes de apresentar a resolução do desafio, segue um entendimento de contexto sobre o diagrama UML apresentado anteriormente

**Classes e Relacionamentos**

1) **Historico()**
   - ***Métodos***:
     - **adicionar_transacao(transacao *<kbd>Transacao()</kbd>*)**: Adiciona uma transação ao histórico
   - ***Relacionamentos***:
     - Uma instância de <kbd>Historico()</kbd> tem um relacionamento 1:N com <kbd>Transacao()</kbd>, ou seja, um histórico pode ter várias transações

2) **Transacao(Interface)**
   - ***Métodos***:
     - **registrar(conta *<kbd>Conta()</kbd>*)**: Método para registrar uma transação em uma conta
   - ***Relacionamentos***:
     - <kbd>Transacao()</kbd> é uma interface implementada pelas classes <kbd>Deposito()</kbd> e <kbd>Saque()</kbd>

3) **Deposito()**
   - ***Atributos***:
     - **valor**: Valor do depósito (formato: *float*)
   - ***Métodos***:
     - Herda o método **registrar** da interface <kbd>Transacao()</kbd>
   - ***Relacionamentos***:
     - É uma especialização (herança) de <kbd>Transacao()</kbd>

4) **Saque()**
   - ***Atributos***:
     - **valor**: Valor do saque (formato: *float*)
   - ***Métodos***:
     - Herda o método **registrar** da interface <kbd>Transacao()</kbd>
   - ***Relacionamentos***:
     - É uma especialização (herança) de <kbd>Transacao()</kbd>

5) **Conta()**
   - ***Atributos***:
     - **saldo**: Saldo da conta (formato: *float*);
     - **numero**: Número da conta (formato: *int*);
     - **agencia**: Agência da conta (formato: *str*);
     - **cliente**: Cliente associado à conta (formato: <kbd>Cliente()</kbd>);
     - **historico**: Histórico de transações da conta (formato: <kbd>Historico()</kbd>)
   - ***Métodos***:
     - **saldo() return *float***: Retorna o saldo da conta;
     - **nova_conta(cliente *<kbd>Cliente()</kbd>*, numero *int*) return *<kbd>Conta()</kbd>***: Cria uma nova conta para um cliente;
     - **sacar(valor *float*) return *bool***: Realiza um saque na conta;
     - **depositar(valor *float*) return *bool***: Realiza um depósito na conta
   - ***Relacionamentos***:
     - Uma instância de <kbd>Conta()</kbd> está associada a um cliente;
     - Uma instância de <kbd>Conta()</kbd> possui um histórico que mantém um registro das transações;
     - Um cliente pode ter várias contas

6) **Cliente()**
   - ***Atributos***:
     - **endereco**: Endereço do cliente (formato: *str*);
     - **contas**: Lista de contas do cliente (formato: *list*)
   - ***Métodos***:
     - **realizar_transacao(conta: *<kbd>Conta()</kbd>*, transacao: *<kbd>Transacao()</kbd>*)**: Realiza uma transação em uma conta específica;
     - **adicionar_conta(conta: *<kbd>Conta()</kbd>*)**: Adiciona uma conta à lista de contas do cliente
   - ***Relacionamentos***:
     - Um cliente pode ter várias contas;
     - O cliente realiza transações

7) **ContaCorrente()**
   - ***Atributos***:
     - **limite**: Limite de crédito da conta corrente (formato: *float*);
     - **limite_saques**: Limite de saques permitido (formato: *int*)
   - ***Relacionamentos***:
     - É uma especialização (herança) de <kbd>Conta()</kbd>.

8) **PessoaFisica**()
   - ***Atributos***:
     - **cpf**: CPF do cliente (formato: *str*);
     - **nome**: Nome do cliente (formato: *str*);
     - **data_nascimento**: Data de nascimento do cliente (formato: *date*)
   - ***Relacionamentos***:
     - É uma especialização (herança) de <kbd>Cliente()</kbd>

<br>

**Relacionamentos no Diagrama**

1) **<kbd>Histórico()</kbd> <-> <kbd>Transacao()</kbd>**:
   - Um historico pode conter múltiplas transações

2) **<kbd>Conta()</kbd> <-> <kbd>Cliente()</kbd>**:
   - Uma conta está associada a um único cliente;
   - Um cliente pode ter múltiplas contas

3) **<kbd>Transacao()</kbd> <-> <kbd>Conta()</kbd>**:
   - Uma transação é realizada em uma conta específica


<br>

**Conceitos de POO encontrados no diagrama**



~~~Python
~~~
