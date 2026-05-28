# Projeção de Sinais em Subespaços

## Problema

Um programa de computador que transforme um sinal $x\in\mathbb{R}^{n}$ em uma aproximação x, contida em um subespaço U. Dada uma base B para este subespaço, obtenha $[\tilde{x}]_{B}\in\mathbb{R}^{k}$ onde $k=dim(\mathcal{U})$.

## Solução

O problema propõe encontrar a melhor aproximação de um sinal $\mathbf{x} \in \mathbb{R}^n$ contida em um subespaço $\mathcal{U}$ de dimensão $k$ (onde $k < n$). Essa "melhor aproximação" pode ser interpretada como a projeção ortogonal do vetor $\mathbf{x}$ sobre o subespaço $\mathcal{U}$.

Como o sinal aproximado $\tilde{\mathbf{x}}$ pertence ao subespaço $\mathcal{U}$, ele pode ser descrito como uma combinação linear dos vetores da matriz base $B$. Os coeficientes dessa combinação linear são exatamente o vetor de coordenadas $[\tilde{\mathbf{x}}]_B$. Portanto:

$$\tilde{\mathbf{x}} = B[\tilde{\mathbf{x}}]_B$$

Para que $\tilde{\mathbf{x}}$ seja a melhor aproximação possível, a diferença entre o sinal original e a sua aproximação (o vetor de erro) deve ser ortogonal ao subespaço $\mathcal{U}$.

$$\text{Vetor de erro: } \mathbf{e} = \mathbf{x} - \tilde{\mathbf{x}} = \mathbf{x} - B[\tilde{\mathbf{x}}]_B$$

Para que o erro $\mathbf{e}$ seja ortogonal a todo o subespaço, ele deve ser ortogonal a todos os vetores da base $B$. Isso significa que a multiplicação da matriz transposta de $B$ pelo vetor de erro deve resultar no vetor nulo:

$$B^T\mathbf{e} = \mathbf{0}$$

Substituindo a definição do nosso vetor de erro na equação acima:

$$B^T(\mathbf{x} - B[\tilde{\mathbf{x}}]_B) = \mathbf{0}$$

Aplicando a propriedade distributiva da multiplicação de matrizes:

$$B^T\mathbf{x} - B^TB[\tilde{\mathbf{x}}]_B = \mathbf{0}$$

Agora, isolamos o termo que contém a nossa incógnita, $[\tilde{\mathbf{x}}]_B$:

$$B^TB[\tilde{\mathbf{x}}]_B = B^T\mathbf{x}$$

Neste ponto, devemos resolver um sistema de equações lineares. Para encontrar o vetor de coordenadas $[\tilde{\mathbf{x}}]_B$, o objetivo é solucionar este sistema matricial, onde a matriz dos coeficientes é $B^TB$ e o vetor de termos independentes é $B^T\mathbf{x}$.
