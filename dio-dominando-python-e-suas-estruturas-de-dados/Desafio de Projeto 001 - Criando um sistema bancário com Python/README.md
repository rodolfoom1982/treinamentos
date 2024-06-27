# Desafio de Projeto 001 - Criando um sistema bancário com Python

![Static Badge](https://img.shields.io/badge/Status_Projeto:-Concluído_(16/Jun/2024)-green)

![Static Badge](https://img.shields.io/badge/Python-blue)

<br>

## Índice

- [Objetivo](#Objetivo)
- [Requisitos](#Requisitos)
- [Resolução](#Resolução)

<br>

## Objetivo

Desenvolver um sistema bancário utilizando a linguagem Python

<br>

## Requisitos

1) Para a primeira versão do sistema, implementar apenas 3 operações: *depósito*, *saque* e *extrato*
2) **Operação de Depósito**:
   - Permitir o depósito de valores positivos;
   - Todos os depósitos devem ser armazenados em uma variável e exibidos na operação de extrato;
4) **Operação de Saque**:
   - O sistema deve permitir a realização de, no máximo, 3 saques diários, com limite de R$ 500,00;
   - Caso o usuário não tenha saldo em conta, o sistema deve exibir uma mensagem informando que não será possível sacar o dinheiro por falta de saldo;
   - Todos os saques devem ser armazenados em uma variável e exibidos na operação de extrato;
5) **Operação de Extrato**:
   - Deve listar todos os depósitos e saques realizados na conta;
   - Ao final da listagem deve ser exibido o saldo atual da conta;
   - Se o extrato estiver em branco, exibir a mensagem: *Não foram realizadas movimentações*
   - Os valores devem ser exibidos utilizando o formato R$ xxx.xx (Ex.: para 1500.45, exibir R$ 1500.45)

<br>

## Resolução

~~~Python
dash = '#' * 60 # Barra para organizar o código

# Menu para ser apresentado ao usuário
menu = f"""
Escolha uma das opções abaixo:\n
[D] - Depositar
[S] - Sacar
[E] - Extrato
[Q] - Sair\n
"""

LIMITE_SAQUE_DIARIO = 3 # Limite de saques diários permitido
LIMITE_OPERACAO_SAQUE = float(500) # Valor máximo permitido por operação saque
saquesRealizados = 0 # Acumulado de saques já realizados
saldo = float(0) # Saldo inicial
transacoes = [] # Lista de operações realizadas

while True:

  # Exbir o menu e solicitar ao usuário que informe a opção desejada
  print(f'\n{dash}')
  opcao = input(menu)
  
  # Operação de Depósito
  if opcao.upper() == 'D':

    while True:

      # Solicita o valor do depósito
      valor = input('\nInforme o valor que deseja depositar (Para sair, digite [Q]): ')

      try:
        valor = round(float(valor), 2)

        # Realiza o depósito
        if valor > 0:
          saldo += valor # Incrementa o saldo
          transacoes.append(['Depósito', valor]) # Armazena a transação
          print(f'\t >>> Depósito realizado com sucesso! Saldo disponível: R$ {saldo:.2f}')

        # Sinaliza erro se o valor informando for <= 0
        else:
          print('\t >>> E R R O: Insira um valor maior que 0 (zero)!')

      except:
        # Sai da operação de depósito se o valor informado for 'q' ou 'Q'
        if str(valor).upper() == 'Q':
          break
        
        # Sinaliza erro se o valor informando não for numérico
        else:
          print('\t >>> E R R O: Insira um valor numérico válido!')
  

  # Operação de Saque
  elif opcao.upper() == 'S':

      while True:
        # Impede novos saques se o limite diário for excedido
        if saquesRealizados >= LIMITE_SAQUE_DIARIO:
          print('\nVocê ultrapassou a quantidade de 3 saques permitidos por dia')
          break

        else:
          # Solicita o valor do saque
          valor = input('\nInforme o valor que deseja sacar (Para sair, digite [Q]): ')

          try:
            valor = round(float(valor), 2)

            # Impede o saque se não houver saldo suficente
            if valor > saldo:
              print(f'\t >>> E R R O: Seu saldo disponível (R$ {saldo:.2f}) é insuficiente para esta operação!')
            
            # Realiza o saque
            elif valor > 0 and valor <= LIMITE_OPERACAO_SAQUE:
              saldo -= valor # Decrementa o saldo
              transacoes.append(['Saque', valor * -1]) # Armazena a transação
              saquesRealizados += 1 # Incrementa a quantidade de saques realizada
              print(f'\t >>> Saque realizado com sucesso! Saldo disponível: R$ {saldo:.2f}')

            # Impede o saque se não houver saldo suficente
            elif valor > LIMITE_OPERACAO_SAQUE:
              print(f'\t >>> E R R O: Seu limite de saque é de R$ {LIMITE_OPERACAO_SAQUE:.2f} por operação!')
            
            # Sinaliza erro se o valor informando for <= 0
            else:
              print('\t >>> E R R O: Insira um valor maior que 0 (zero)!')

          except:
            # Sai da operação de saque se o valor informado for 'q' ou 'Q'
            if str(valor).upper() == 'Q':
              break
            
            # Sinaliza erro se o valor informando não for numérico
            else:
              print('\t >>> E R R O: Insira um valor numérico válido!')

  
  # Operação de Extrato
  elif opcao.upper() == 'E':

    print('\nExtrato:')
    print('-' * 100)

    # Sinalizar se não houver transações
    if len(transacoes) == 0:
      print('\nNão foram realizadas movimentações!')
    
    # Detalha as transações
    else:
      for i in transacoes:
        print(f'{i[0]} {"." * (30 - len(i[0]))} R$ {i[1]:.2f}')
      print('-' * 50)
      print(f'Saldo disponível {"." * (30 - len("Saldo disponível"))} R$ {saldo:.2f}')
  
  
  # Operação de Saída do Programa
  elif opcao.upper() == 'Q':
    print(f'\n{dash}\n\nVolte Sempre!!!!')
    break
  

  # Operações não reconhecidas pelo sistema
  else:
    print('Opção inválida, tente novamente!')
~~~
