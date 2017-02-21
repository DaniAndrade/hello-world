'''
    A GFG precisa descobrir quanto de vale transporte esta gastando por funcionário por período.
    Alguns funcionários utilizam apenas ônibus (R$ 3,80) e outros dependem de integração (R$ 5,92)
 
'''

qtd_funcionarios = int (input('Quantos funcionários há atualmente na GFG? '))
qtd_onibus = int (input('Dessa quantidade, quantos utilizam apenas ônibus? '))
qtd_integracao = qtd_funcionarios - qtd_onibus
valor_onibus = float (input('Valor atual do ônibus: R$ '))
valor_integracao = float (input('Valor atual da integração: R$ '))
ida_volta = int (input('Considerar ida e volta? (Sim digite 1) (Não digite 2): '))
if ida_volta==1: #Cálculo total considerando ida e volta
    dias_calculo = int (input ('Quantos dias para o cálculo? '))*2
else: #Cálculo total considerando ida
    dias_calculo = int (input ('Quantos dias para o cálculo? '))
total_onibus = qtd_onibus*valor_onibus*dias_calculo 
total_integracao = qtd_integracao*valor_integracao*dias_calculo

print ('O total de', qtd_onibus, 'funcionários utilizam ônibus ao custo de R$ %.2f.' %total_onibus)
print ('Já' , qtd_integracao, 'funcionários utilizam integração ao custo total de R$ %.2f.' %total_integracao)
