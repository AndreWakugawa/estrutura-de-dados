1.1.1 Escreva a documentação correta da função abaixo.

int soma (int n, int v[]) {
	int i, x = 0;
	for (i = 0; i < n; i++) x += v[i];
	return x; }

A função abaixo recebe o valor de um inteiro n>=1 e um vetor de inteiros v 
e retorna a soma de todos os elementos de v[0..n-1]

------
1.1.2 Escreva a documentação correta da função abaixo.

int onde (int x, int v[], int n) {
	int j = 0;
	while (j < n && v[j] != x) j += 1;
	return j; }

 A função abaixo recebe um inteiro x, um vetor de inteiros v e um inteiro n<=v.length.
Ele retorna a quantidade de elementos de v diferentes de x até o limite de n-1 ou algum
elemento se igualar a x.

-------
1.1.3 Critique a seguinte documentação de uma função:

"Esta função recebe números inteiros p, q, r, s e devolve a média aritmética de p, q, r."

A documentação informa que a função recebe a informação inutil do inteiro s que não é utilizada.

------
1.1.4 Critique a seguinte documentação de uma função:

"Esta função recebe números inteiros p, q, r tais que p <= q <= r e devolve a média aritmética dos três números."

A documentação é redundante e pode ser resumida em:
"Esta função recebe números inteiros p <= q <= r e devolve a média aritmética dos três números."
