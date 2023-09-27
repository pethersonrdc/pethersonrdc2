# Dicionario de Alunos em Python

- 👋  ole meu nome é petherson henrique -- @pethersonrdc2
#⭐⭐Segue nossa Ac completa⭐⭐#

#Dicionário dos alunos
alunos = {}

opcao = 1
menu = [1,2,3,4,5,6]
while(opcao in menu ):
        opcao = int(input("""
    Por favor, digite a opção que você deseja:

      1 - Adicionar novo aluno
      2 - Remover aluno
      3 - Adicionar nota
      4 - Calcular média
      5 - Exibir notas do aluno
      6 - Rank dos alunos
      7 - Sair

    Insira o número: """))

        match opcao:

            case 1: # Adicionar novo aluno
                incluir = 's'
                while incluir == 's':
                    nome = input('Informe o nome: ')
                    alunos [nome] = [] #insere no dicionario
                    incluir = input('Deseja incluir mais um aluno? s ou n ')

            case 2: #Remover aluno
                print(alunos.keys())
                deletado = input('Qual aluno você deseja deletar? ')
                alunos.pop(deletado)


            case 3: #Adicionar nota
                incluir_nova_nota_aluno ='s'
                while incluir_nova_nota_aluno =='s':
                    nome_aluno = input('Informe o nome do aluno: ')
                    if nome_aluno in alunos:
                        cont = 1
                        notas = []
                        while cont <= 4:
                            n = input('Inserir a nota: ')
                            notas.append(n)
                            cont += 1
                        alunos [nome_aluno] = notas
                    else:
                        print('Vá para o menu opção 1')
                    incluir_nova_nota_aluno = input('deseja incluir nota de outro aluno: s/n? ')
                    print(alunos)


            case 4: #Calcular média
                print(alunos.keys())
                calculado = input('De qual aluno você deseja calcular a média? ').lower()
                notas = alunos[calculado] = []
                media = sum([notas]) / len([notas])
                print(media)


            case 5: #Exibir notas do aluno
                print(alunos.keys())
                exibir_input = input('Qual aluno você deseja exiber as notas? ')
                exibir = alunos[exibir_input]
                print(exibir)


            case 6: #Rank dos alunos
                total_por_aluno = []
                nomes_alunos = []

                for aluno, notas in alunos.items():
                    somatoria = sum(notas)
                    total_por_aluno.append(somatoria)
                    nomes_alunos.append(aluno)

                maior = max(total_por_aluno)
                indice = total_por_aluno.index(maior)
                print(f'Melhor aluno: {nomes_alunos[indice]}, {maior}')

                menor = min(total_por_aluno)
                indice = total_por_aluno.index(menor)
                print(f'Pior aluno: {nomes_alunos[indice]}, {menor}')



            case 7: # Sair
                opcao == 7
                print(opcao)
                break

            case _:
                print('Opção inválida, tente novamente!')

print('Tchau , até breve!')
<!---
pethersonrdc/pethersonrdc is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
