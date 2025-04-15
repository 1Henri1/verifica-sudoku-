import time

inicio = time.time()
def compativel(Matriz):
    tam = len(Matriz)
    somalinha=0
    somacoluna=0
    for i in range(tam):
        somalinha=0
        somacoluna=0
        for j in range(tam):
            if not(0<Matriz[i][j]<=tam or 0<Matriz[j][i]<=tam):
                return False
            somalinha+=Matriz[i][j]
            somacoluna+=Matriz[j][i]
        if somacoluna != (tam*(tam+1))/2 or somalinha != (tam*(tam+1))/2:
            return False
    for i in range(tam):
        for j in range(i+1,tam):
            if Matriz[i][i] == Matriz[j][i] or Matriz[i][i] == Matriz[i][j]:
                return False
    return True

n=1000
linha = "0 "*n
coluna = (linha+";")*n
coluna = coluna[:-1]
matriz = [[int(y) for y in x.split()] for x in coluna.split(";")]
for i in range(n):
    for j in range(n):
        matriz[i][j]= (j-i)%n+1
print(compativel(matriz))
fim = time.time()
print(fim-inicio)
