## Calculadora de IMC

![header](https://www.crouse.org/wp-content/uploads/2019/01/BMI-Crouse-Weightloss-Surgery.jpg)

## Licence

????????????????/https://github.com/JeffersonLCXaxa/Combust-veis-2013-a-2021/blob/main/LICENCE

#Função para calcular o imc
def calcular_imc(peso, altura):
    imc = peso / (pow(altura, 2))
    return imc

#Função para classificar (condições) o imc
def classificar_imc(imc):
    if imc < 18.5:
        return 'Baixo peso'
    elif 18.5 <= imc < 24.9:
        return 'Peso Normal'
    elif 25 <= imc < 29.9:
        return 'Excesso de Peso'
    elif 30 <= imc < 34.9:
        return 'Obesidade de 1º grau'
    elif 35 <= imc < 39.9:
        return 'Obesidade de 2º grau'
    elif imc >= 40:
        return 'Obesidade de 3º grau'

#Informação de limitação da aplicação e fonte da informação
print('\nATENÇÂO\nEm crianças e adolescentes o IMC também é medido, mas as faixas de peso normal, sobrepeso ou obesidade não são as mesmas dos adultos. Em corpos em fase de crescimento, o cálculo leva em conta a idade e varia também para meninos ou meninas. \n\nOs médicos usam gráficos aprovados pela Organização Mundial de Saúde. Neles, o IMC infantil é calculado a partir de linhas que correspondem a índices estatísticos chamados de percentil e escore-Z. Por isso, é fundamental buscar ajuda profissional para o diagnóstico da obesidade infantil.')
print('\nFONTE\nhttps://www.saudenaosepesa.com.br/diagnostico.html?gclid=Cj0KCQjwsIejBhDOARIsANYqkD3KFNoVA_t5k3Rc_XYADGMmZQP3DXB6TmZv9v4hKy821KKTETL0nR8aAoe8EALw_wcB')

#Variável de controle 1
execucao = True

#Looping de execução da aplicação
while execucao:
    try:

        #Entrada de dados (peso e altura) e aplica a função de calculo
        peso = float(input('\nInforme seu peso em kg (Ex.: 100.00): '))
        altura = float(input('Informe sua altura em metros (Ex.: 1.76): '))
        imc = calcular_imc(peso, altura)

        #Resultado do calculo das entradas (imc)
        print(f'\nSeu IMC é {imc:.2f}')

        #Aplica a função de classificação no imc e apresenta o resultado
        print(f'Sua classificação é: {classificar_imc(imc)}')

        #Variável de controle 2
        opcao = str(input('\nGostaria de fazer um novo cálculo? [S/N] ')).upper()

        #Looping para tratar entradas diferentes de 'S' ou 'N'
        while opcao != 'S' and opcao != 'N':
            opcao = str(input('\nGostaria de fazer um novo cálculo? [S/N] ')).upper()

        #Encerramento da execução bem sucedida
        if opcao == 'N':
            execucao = False
            print('Obrigado e até mais!')

    #Tratamento de erro
    except:
        print('ERROR: Informação inválida.')
    
## Project authorship

Jefferson Luiz da Costa Xaxá

LinkedIn: https://www.linkedin.com/in/jefferson-xax%C3%A1-815516b0/
