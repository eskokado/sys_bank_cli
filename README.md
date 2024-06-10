# Sistema bancário ficticio

O sistema bancário criado é um programa interativo que permite aos usuários realizar operações bancárias básicas e gerenciar contas e clientes. Ele é composto por várias funções modulares para facilitar a manutenção e a expansão do código. Abaixo está uma visão geral das funcionalidades e da estrutura do sistema:

## Funcionalidades Principais:
- Cadastro de Clientes:

  - Descrição: Permite cadastrar novos clientes no sistema.
  - Dados Necessários: Nome, data de nascimento, CPF e endereço.
  - Validação: Verifica se o CPF já está cadastrado para evitar duplicidade.
- Cadastro de Contas Bancárias:

  - Descrição: Cria uma nova conta bancária associada a um cliente existente.
  - Dados Necessários: CPF do cliente.
  - Detalhes da Conta: Cada conta tem uma agência fixa ("0001") e um número sequencial único.
- Operação de Depósito:

  - Descrição: Permite aos clientes depositar dinheiro em suas contas.
  - Dados Necessários: Valor do depósito.
Validação: O valor do depósito deve ser positivo.
- Operação de Saque:

  - Descrição: Permite aos clientes sacar dinheiro de suas contas.
  - Dados Necessários: Valor do saque.
Validação: O saque deve atender aos seguintes critérios:
    - Não exceder o saldo disponível.
    - Não exceder o limite de saque.
    - Não exceder o número máximo de saques permitidos por dia.
- Visualização de Extrato:

  - Descrição: Exibe o histórico de transações e o saldo atual da conta.
  - Detalhes: Mostra todas as operações realizadas (depósitos e saques) e o saldo atual.
## Menu Interativo:

### Opções Disponíveis:
- [d] Depositar
- [s] Sacar
- [e] Extrato
- [nu] Novo Usuário
- [nc] Nova Conta
- [q] Sair
## Estrutura do Programa:
### Listas para Armazenamento:

- usuarios: Armazena os dados dos clientes.
- contas: Armazena os dados das contas bancárias.
### Funções Modulares:

- cadastrar_cliente(nome, data_nascimento, cpf, endereco): Cadastra um novo cliente.
- cadastrar_conta(cpf): Cria uma nova conta bancária associada a um cliente.
- sacar(*, saldo, valor, extrato, limite, numero_saques, - limite_saques): Realiza a operação de saque.
- depositar(saldo, valor, extrato): Realiza a operação de depósito.
- exibir_extrato(saldo, *, extrato): Exibe o extrato e o saldo atual.
