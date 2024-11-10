while True:  # Inicia um loop infinito
    try: #tenta rodar o bagulho que pode dar ruim
        num1 = int(input('Me diga um numero: ')) #pede o numero1 e armazena
        num2 = int(input('Me diga outro numero: ')) #pede o numero2 e armazena
        op = input('Qual operaçao deseja fazer? (+, -, *, /): ') #armazena a operacao

        #Realiza a operação escolhida pelo usuário
        if op == '+':
            result = num1 + num2
        elif op == '-':
            result = num1 - num2
        elif op == '*':
            result = num1 * num2
        elif op == '/':
            if num2 == 0:
                print('nao é possivel dividir por 0, tente novamente')
                continue
            result = num1 / num2
        else:
            print ('Você nao colocou uma operaçao valida, por favor tente novamente!')
            continue
        
        print (f'resultado: {result}') #exibe a soma
        break #sai do loop quando der tudo certo

    except ValueError: #se der ruim, desenrola e não deixa quebrar o rolê
        print ('Você digitou um valor invalido, Por favor, insira um número inteiro.')      
