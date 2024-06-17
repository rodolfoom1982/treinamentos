# Desafio de Projeto 002 - Otimizando o sistema bancário com funções Python

## Objetivo

Otimizar o código do sistema bancário criado no [Desafio de Projeto 001](https://github.com/rodolfoom1982/treinamentos/tree/main/dio-dominando-python-e-suas-estruturas-de-dados/Desafio%20de%20Projeto%20001%20-%20Criando%20um%20sistema%20banc%C3%A1rio%20com%20Python), utilizando funções em Python, deixando o código mais modularizado

<br>

## Requisitos

1) Transformar as 3 operações criadas anteriormente (*depósito*, *saque* e *extrato*) em funções;
2) Criar 2 novas operações em forma de função:
   - *Criar usuário (cliente do banco)*;
   - *Criar conta corrente*;
3) Cada função vai ter sua própria regra de passagem de argumentos e deve ser seguida à risca;
4) A forma de chamar cada função e seu respectivo retorno pode ser definido da melhor forma desejada;
5) **Função *saque***:
   - Deve receber os argumentos por nome (*keyword only*);
   - Sugestão de argumentos: *saldo*, *valor*, *extrato*, *limite*, *numero_saques*, *limite_saques*;
   - Sugestão de retorneo: *saldo* e *extrato*;
6) **Função *depósito***:
   - Deve receber os argumentos por posição (*positional only*);
   - Sugestão de argumentos: *saldo*, *valor*, *extrato*;
   - Sugestão de retorneo: *saldo* e *extrato*;
7) **Função *extrato***:
   - Deve receber os argumentos por posição e nome (*positional only* e *keyword only*);
   - Argumento posicional: *saldo*;
   - Argumento nomeado: *extrato*;
8) **Função *criar usuário***:
   - O programa deve armazenar os usuários em uma lista;
   - Um usuário é composto por: *nome*, *data de nascimento*, *cpf* e *endereço*;
   - O endereço é um string com o formato: *"logradouro, numero - bairro - cidade / sigla estado"*;
   - Devem ser armazenados somente os números do CPF;
   - Não se pode cadastar 2 ou mais usuários com o mesmo CPF;
9) **Função *criar conta corrente***:
   - O programa deve armazenar as contas em uma lista;
   - Uma conta é composta por: *agência*, *número da conta* e *usuário*;
   - O *número da conta* é sequencial, iniciando em 1;
   - O número da agência é fixo: *"0001"*
   - O usuário pode ter mais de uma conta, mas uma conta pertence a somente um usuário;
   - Para vincular um usuário a uma conta, filtre a lisa de usuários, buscando o número do CPF informado para cada usuário na lista

<br>

## Resolução

~~~Python
~~~
