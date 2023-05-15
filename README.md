## BMI calculator

![header](https://www.crouse.org/wp-content/uploads/2019/01/BMI-Crouse-Weightloss-Surgery.jpg)

## Licence

https://github.com/JeffersonLCXaxa/Calculadora_de_IMC/blob/main/LICENSE

## Technologies Used:
<table>
    <tr>
        <td>Visual Studio Code</td>
        <td>Python</td>
    </tr>
    <tr>
        <td>v1.77</td>
        <td>v3.10.9</td>
    </tr>
</table>

## Starting code

- Function to calculate BMI

        def calcular_imc(peso, altura):
            imc = peso / (pow(altura, 2))
            return imc

- Function to sort (conditions) the imc

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

- Application limitation information and source of information

        print('\nATTENTION\nIn children and adolescents, BMI is also measured, but the ranges for normal weight, overweight or obesity are not the same as for adults. In bodies in the growth phase, the calculation takes into account age and also varies for boys or girls. \n\nDoctors use charts approved by the World Health Organization. In them, children's BMI is calculated from lines that correspond to statistical indices called percentiles and Z-scores. Therefore, it is essential to seek professional help for the diagnosis of childhood obesity.')

        print('\nSOURCE OF INFORMATION\nhttps://www.saudenaosepesa.com.br/diagnostico.html?gclid=Cj0KCQjwsIejBhDOARIsANYqkD3KFNoVA_t5k3Rc_XYADGMmZQP3DXB6TmZv9v4hKy821KKTETL0nR8aAoe8EALw_wcB')

- Control variable 1
        
        execucao = True

- Application execution loop
        
        while execucao:
            try:

- Input data (weight and height) and apply the calculation function
                        
                        peso = float(input('\nEnter your weight in kg (such as: 100.00): '))
                        altura = float(input('Informe sua altura em metros (such as: 1.76): '))
                        imc = calcular_imc(peso, altura)

- Result of the calculation of entries (imc)
                        
                        print(f'\nYour BMI is {imc:.2f}')

- Applies the sorting function to the imc and displays the result
                        
                        print(f'Your rating is: {classificar_imc(imc)}')

- Control variable 2
                        
                        opcao = str(input('\nI would like to do a new calculation? [Y/N] ')).upper()

- Looping to handle inputs other than 'Y' or 'N'
                        
                        while opcao != 'Y' and opcao != 'N':
                            opcao = str(input('\nI would like to do a new calculation? [Y/N] ')).upper()

- Successful run closure
                        
                        if opcao == 'N':
                            execucao = False
                            print('Thank you and see you!')

- Error Handling
            
            except:
                print('ERROR: Informação inválida.')
    
## Project authorship

Jefferson Luiz da Costa Xaxá

LinkedIn: https://www.linkedin.com/in/jefferson-xax%C3%A1-815516b0/
