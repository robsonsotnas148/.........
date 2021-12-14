# jogodeadivinhacao
print('===================================')
print('bem vindo ao jogo de adivinhação!!')
print('===================================')

numerosecreto = 4
total_de_tentativas = 3


for rodada in range(1,total_de_tentativas + 1) :
    print('tentativa {} de {}'.format(rodada,total_de_tentativas))
    chute = int(input('digite um numero entre 1 e 100:'))
    if(chute < 1 or chute > 100):
        print('Número invalido, você deve digitar um número entre 1 e 100')
        continue
    print('você chutou', chute)
    acertou = chute == numerosecreto
    maior = chute > numerosecreto
    menor = chute < numerosecreto
    if (acertou):
     print('parabens, você acertou o numero secreto')
     break
    else:
        if(maior):
         print('você errou, seu chute foi maior do que o numero secreto!!')
        elif(menor):
            print('você errou, seu chute foi menor do que o numero secreto.')
print('fim de jogo')
