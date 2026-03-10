# Qualquer-coisa
# calculadora.py

def adicao(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b == 0:
        return "Erro! Divisão por zero."
    return a / b

def calculadora():
    print("--- Calculadora Simples ---")
    print("Selecione a operação:")
    print("1. Adição (+)")
    print("2. Subtração (-)")
    print("3. Multiplicação (*)")
    print("4. Divisão (/)")

    escolha = input("Digite sua opção (1/2/3/4): ")

    if escolha in ['1', '2', '3', '4']:
        try:
            num1 = float(input("Digite o primeiro número: "))
            num2 = float(input("Digite o segundo número: "))

            if escolha == '1':
                print(f"Resultado: {num1} + {num2} = {adicao(num1, num2)}")
            elif escolha == '2':
                print(f"Resultado: {num1} - {num2} = {subtracao(num1, num2)}")
            elif escolha == '3':
                print(f"Resultado: {num1} * {num2} = {multiplicacao(num1, num2)}")
            elif escolha == '4':
                print(f"Resultado: {num1} / {num2} = {divisao(num1, num2)}")
        except ValueError:
            print("Erro: Entrada inválida. Digite números.")
    else:
        print("Opção inválida.")

if __name__ == "__main__":
    while True:
        calculadora()
        contar = input("Deseja realizar outro cálculo? (s/n): ")
        if contar.lower() != 's':
            break
