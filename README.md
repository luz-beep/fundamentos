#include <iostream>
using namespace std;

int calcular(int n);

int main()
{
	int n, suma;
	cout << "Ingrese el numero hasta el que desee sumar: ";
	cin >> n;
	suma = calcular(n);
	cout << "La suma de los numeros es  " << n << " es: " << suma;
}
int calcular(int n) {
	int s = 0, i = 1;
	while (i <= n) {
		s=s+i;
		i++;
	}
	return s;
}
