# problema-5---fase-5
# Matriz de horas trabajadas: 4 recursos x 5 días
horas_por_dia = [
    [8, 8, 8, 8, 9],   # ANA
    [7, 8, 8, 6, 7],   # CARLOS
    [9, 9, 8, 8, 8],   # MARÍA
    [8, 8, 7, 8, 8],   # JUAN
]

ESTANDAR_HORAS = 40

print('--'*30)
print('        HORAS TRABAJADAS POR RECURSO EN LA SEMANA    ')
print('=='*30) 
print(f'|             Horas estándar por semana: {ESTANDAR_HORAS}                |')
print('=='*30) 
print()
print('NOMBRE  |  HORAS TRABAJADAS | TOTAL SEMANA | ESTADO')
print('--'*30) 

for nombre, horas_dias in zip(['ANA     ', 'CARLOS  ', 'MARÍA   ', 'JUAN    '], horas_por_dia):
    total_semana = sum(horas_dias)
    excede = total_semana > ESTANDAR_HORAS
    estado = 'Sobretiempo' if excede else 'Horario Estándar'
    print(f'{nombre}:  {horas_dias}  =   {total_semana} horas   | ({estado})')

print('--'*30)
