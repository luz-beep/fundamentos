#include <iostream>
#include <math.h>

using namespace std;

int main(){
    int numero  , digito , pares=0, impares=0 , p=0 , i=0;
    do {
        cout <<"ingrese el numero :";
        cin>>numero ;
    }while (numero<=0);
    while(numero>0)
    {
        digito=numero % 10;
        if (digito%2 ==0){
            pares=pares +1;
            p=p+digito;
        }
        else {
            impares=impares+1;
            i=i+digito ;
        }
        numero = numero / 10;
    }
    cout<< "la cantidad de numeros pares es "<< pares << endl;
    cout<< "la suma de numeros pares es "<< p << endl;
    cout<< "la cantidad de numeros impares es :"<< impares<<endl;
    cout<< "la suma de numeros impares es "<< i << endl;

 return 0;

}
