# Sistema Bancário

## Objetivo

Este projeto visa criar um sistema bancário simples com base em conceitos de Programação Orientada a Objetos (POO), com a possibilidade de interação via terminal ou interface gráfica utilizando Tkinter.

## Funcionalidades

- **Cadastro de contas bancárias**
- **Diferentes tipos de contas:** Conta Corrente e Conta Poupança
- **Operações bancárias:** Depósitos, Saques, Transferências
- **Gerenciamento de clientes e suas contas**

## Conceitos de POO Aplicados

- **Classes:** As classes `Conta`, `Cliente` e `Banco` representam as entidades principais do sistema bancário.
- **Herança:** A classe `ContaCorrente` e `ContaPoupança` herdam de `Conta`, cada uma com suas características específicas.
- **Polimorfismo:** O método `sacar()` é implementado de forma diferente nas classes `ContaCorrente` e `ContaPoupança` para atender às regras de cada tipo de conta.
- **Encapsulamento:** Atributos como `saldo` e `senha` são protegidos para garantir que não sejam acessados diretamente fora da classe.

## Como Rodar o Projeto
...
### Pré-requisitos

- Python 3.x

### Instalação

1. Clone o repositório:
    ```bash
    git clone https://github.com/davidtanaka/projeto-conta-bancaria-poo.git
    ```
2. Navegue até o diretório do projeto:
    ```bash
    cd projeto-conta-bancaria-poo 
    ```

### Execução

1. **Modo Terminal**: Para rodar o sistema no terminal, basta executar:
    ```bash
    python main.py
    ```

## Estrutura do Projeto

- `main.py`: Código principal para a operação do sistema bancário via terminal.
- `models.py`: Contém as classes `Conta`, `Cliente`, `Banco`, e as subclasses `ContaCorrente` e `ContaPoupança`.

## Exemplo de Uso

```python
# Criando um cliente
cliente1 = Cliente("João", "12345")

# Criando uma conta corrente para o cliente
conta_corrente = ContaCorrente(cliente1, 1000)

# Depositando dinheiro
conta_corrente.depositar(500)

# Realizando um saque
conta_corrente.sacar(200)

# Consultando saldo
print(conta_corrente.saldo)  # Saída: 1300
