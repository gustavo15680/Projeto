# Projeto

print("\n##########################################################################")
print("         Bem Vindo(a) ao Programa De Auxilio Emergencial Do Governo")
print("##########################################################################\n")

# atributos só para teste
contas = []

while identificar in '123':
    identificar = input('''
    [ 1 ]Voce deseja acessar sua conta?
    [ 2 ]Voce deseja consultar seu auxilio?
    [ 3 ]Voce Deseja Sair? ''')


    if identificar == '1':
        cpf = int(input('Digite seu CPF: '))
        if cpf in contas:
            senha = input('Digite sua senha: ')
            if senha in senha:
                print('Login efetuado com sucesso!!')
                conta = input('''[ 1 ] Voce deseja consultar seu saldo?
                                 [ 2 ] Voce deseja realizar saque?
                                 [ 3 ] Voce realizar deposito?
                                 [ 4 ] Voce deseja realizar transferencia?
                                 [ 5 ] ou Voce deseja Sair?''')


            else:
                print('Senha Incorreta!!')
                senha = input('Digite a senha novamente: ')
        else:
            print('Desculpe, seu CPF não está cadastrado, TENTE NOVAMENTE')
            cpf = int(input('Digite seu CPF: '))

    elif identificar == '2':
        print('Bem Vindo a tela de consulta, responda as perguntas a seguir!')
        maiorDeIdade = input('Voce é maior de idade? (S ou n):')

        if maiorDeIdade in 'SimSIMsim':
            emprego = input('Voce está desempregado? (S ou N):')

            if emprego in 'SimSIMsim':
                renda = input('Sua renda familiar é inferior a R$2,500,00?(S ou N):')
                if renda in 'SimSIMsim':
                    print('Voce Está apto a receber o auxilio emergencial')
                    criarConta = input('''
                    [ 1 ]Voce deseja criar uma conta?
                    [ 2 ] Voce ja tem uma conta?''')
                    if criarConta == '1':
                        contaNovaCpf = input('Digite seu CPF: ')
                        contaNovaSenha = input('Digite sua senha: ')


                elif renda in 'NãonaoNAONÃO':
                    print('\nDesculpe, mas voce não está apto a receber o auxilio')

            elif emprego in 'NãonaoNAONÃO':
                print('\nDesculpe, mas voce não está apto a receber o auxilio')
            else:
                print('Voce digitou errado, TENTE NOVAMENTE')
        else:
            print('\nDesculpe, mas voce não está apto a receber o auxilio')

    elif identificar == '3':
        print('\nVoce Saiu!!')
        break

    else:
        identificar = input('Voce Digitou algo errado, tente novamante: ')
