# najhdadn
def crivo(n, vetor_crivo_inicializado_como_true):
    vetor = vetor_crivo_inicializado_como_true
    vetor[0] = False
    vetor[1] = False

    for i in range(2, n + 1):
        if vetor[i]:
            # achou um primo, vamos marcar todos os múltiplos relevantes
            marcar_multiplos(n, vetor, i)

def marcar_multiplos(n, vetor_crivo, primo):
    for i in range(primo*primo, n + 1, primo):
        vetor_crivo[i] = False
