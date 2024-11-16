#include <iostream>
#include<string>
#define MAX 100
using namespace std;

void cargarall(string vec[], int tel[], int  n);
void mostrarall(string vec[], int tel[], int n);
void burbujaall(string vec[], int tel[], int n);

int main()
{
    int numelem, telef[MAX];
    string nombre[MAX];
    do {
        cout << "ingresar un numero de contactos ";
        cin >> numelem;
    } while ((numelem <= 0) || (numelem > MAX));
    cin.ignore();
    cargarall(nombre, telef, numelem);
    mostrarall(nombre, telef, numelem);
    burbujaall(nombre, telef, numelem);
    mostrarall(nombre, telef, numelem);
    return 0;
}
void cargarall(string vec[], int tel[], int n ) {
        for (int i = 0; i < n; i++) {
            cout << i + 1 << "   NOMBRE :";
            getline (cin, vec[i]);
            cout << "  TELEFONO : ";
            cin >>tel[i];
            cin.ignore();
        }
    }
void mostrarall(string vec[], int tel[], int n) {
    cout << "No. Nombre  \t Telefono " << endl;
    cout << "=========================== " << endl;
    for (int i = 0; i < n; i++)
        cout << i + 1 << " . " << vec[i] << "\t" << tel[i] << endl;
}
void burbujaall(string vec[], int tel[], int n) {
    string auxnom;
    int auxnum;
    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            if (vec[j] < vec[i]) {
                auxnom = vec[j];
                vec[j] = vec[i];
                vec[i] = auxnom;
                auxnum = tel[j];
                tel[j] = tel[i];
                tel[i] = auxnum;
            }
        }
    }
}
