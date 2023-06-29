menu = """
	Escolha a opção desejada:
    -----------------------
	|  [1]  | DEPÓSITO    |
	|---------------------|
	|  [2]  | SAQUE       |
	|---------------------|
	|  [3]  | EXTRATO     |
	|---------------------|
	|  [0]  | SAIR        |
	-----------------------
	=> """

saldo = 0
limite = 500
extrato = ""
numero_saques = 0
LIMITE_SAQUES = 3

while True:
    operacao = input(menu)

    if operacao == "1":
        print("================ DEPÓSITO ================")
        deposito = float(input("Digite o valor a ser depositado: R$"))
        if deposito < 0:
            print("Valor inválido")
            continue
        else:
            saldo += deposito
            print(f"Seu saldo é R${saldo:.2f}")
            extrato += ("Depósito realizado de R${:.2f}\n".format(deposito))
            print("=========================================")

    elif operacao == "2":
        print("================ SAQUE ================")
        if numero_saques >= LIMITE_SAQUES:
            print('Saque indisponível. Você atingiu seu limite de saque do dia')
            continue
        else:
            saque = float(input("Digite o valor a ser sacado: R$"))
            if saque > limite:
                print('Saque indisponível. Você atingiu seu limite de saque do dia.')
                continue
            elif saque > saldo:
                print('Saldo indisponível.')
                continue
            else:
                print('Saque de R${:.2f} realizado'.format(saque))
                saldo -= saque
                print("Seu saldo é R${:.2f} ".format(saldo))
                numero_saques += 1
                extrato += str("Saque realizado de R${:.2f}\n".format(saque))
                print("=========================================")

    elif operacao == "3":
        print("================ EXTRATO ================")
        if extrato == "":
            extrato = "Não foram realizado operações"
        print(extrato)
        extrato = ""
        print("=========================================")
        continue

    elif operacao == "0":
        print("================ SAIR ================")
        print("Volte Sempre.")
        break
