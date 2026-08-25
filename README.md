# print("=== CALCULADORA ===")

while True:
    print("\n1 - Somar")
    print("2 - Subtrair")
    print("3 - Multiplicar")
    print("4 - Dividir")
    print("0 - Sair")

    opcao = input("Escolha uma opção: ")

    if opcao == "0":
        print("Programa encerrado.")
        break

    if opcao not in ["1", "2", "3", "4"]:
        print("Opção inválida!")
        continue

    try:
        n1 = float(input("Digite o primeiro número: "))
        n2 = float(input("Digite o segundo número: "))
    except ValueError:
        print("Digite apenas números.")
        continue

    if opcao == "1":
        resultado = n1 + n2
    elif opcao == "2":
        resultado = n1 - n2
    elif opcao == "3":
        resultado = n1 * n2
    elif opcao == "4":
        if n2 == 0:
            print("Não é possível dividir por zero.")
            continue
        resultado = n1 / n2

    print("Resultado:", resultado)-2