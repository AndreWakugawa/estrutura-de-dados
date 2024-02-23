1.1.1 Escreva a documentação correta da função abaixo.
~~~
int soma (int n, int v[]) {
	int i, x = 0;
	for (i = 0; i < n; i++) x += v[i];
	return x; }
~~~
A função abaixo recebe o valor de um inteiro n>=1 e um vetor de inteiros v 
e retorna a soma de todos os elementos de v[0..n-1]

------
1.1.2 Escreva a documentação correta da função abaixo.
~~~
int onde (int x, int v[], int n) {
	int j = 0;
	while (j < n && v[j] != x) j += 1;
	return j; }
~~~
 A função abaixo recebe um inteiro x, um vetor de inteiros v e um inteiro n<=v.length.
Ele retorna a quantidade de elementos de v diferentes de x até o limite de n-1 ou algum
elemento se igualar a x.

-------
1.1.3 Critique a seguinte documentação de uma função:

"Esta função recebe números inteiros p, q, r, s e devolve a média aritmética de p, q, r."

A documentação informa que a função recebe a informação inutil do inteiro s que não é utilizada.

------
1.1.4 Critique a seguinte documentação de uma função:

"Esta função recebe números inteiros p, q, r tais que p <= q <= r e devolve a média aritmética dos três números."

A documentação é redundante e pode ser resumida em:
"Esta função recebe números inteiros p <= q <= r e devolve a média aritmética dos três números."

------

1.2.1 Mostre que o invariante da função Max vale no início da primeira iteração. Suponha que o invariante vale no início de uma iteração qualquer e mostre que ele vale no
início da iteração seguinte. Suponha que o invariante vale no início da última iteração e deduza daí que a função devolve um elemento máximo do vetor v[0..n-1].
~~~
int Max (int v[], int n) {
	int j, x;
	x = v[0];
	for (j = 1; j < n; j++)
 		/*x é um elemento máximo de v[0..j-1]*/
		if (x < v[j]) x = v[j];
	return x;
 }
~~~
 A função Max, em um contexto de 10 iterações retorna, no início da 10ª iteração, o valor máximo de v[0..10-1] = v[0..9]. Ou seja, o valor máximo das 10 possíveis posições
 Logo, a função, no início da primeira iteração, retorna o valor máximo de v[0..1-1], ou seja v[0..0], um vetor com um único elemento. Assim a função retorna o único elemento que,
 por consequência é o maior do vetor.

 ------

 1.2.2 Qual o invariante do processo iterativo da função soma no Exercício 1.1.1?
~~~
int soma (int n, int v[]) {
	int i, x = 0;
	for (i = 0; i < n; i++) x += v[i];
	return x; }
~~~
x é a soma de todos os elementos de v[0..0-1]

------

1.2.3 Qual o invariante do processo iterativo da função onde no Exercício 1.1.2?
~~~ 
int onde (int x, int v[], int n) {
	int j = 0;
	while (j < n && v[j] != x) j += 1;
	return j; }
~~~
j é o index v[j-1] AAAAA
