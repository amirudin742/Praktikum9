# Praktikum9

Latihan1#Menentukan nilai maximal&minimal menggunkan array

1. Alur algoritmanya

	-Mendeklarasikan int nilai sebagai variabel array

	-mendeklarasikan int a sebagai nilai input

	-int max sebagai nilai maximal

	-int min sebagai nilai minimal

	-membuat perulangan untuk menentukan banyak inputan

for (a=1;a<=5;a++)

        {

        cout<< "Masukan nilai ke-" << a <<": ";

        cin>> nilai[a];

        }

	-menentukan nilai max dan min

for(a=2;a<=5;a++)

    {

        if (nilai[a]<min)

        {

            min=nilai[a];

        }

        else if (nilai[a]>max)

        {

            max=nilai[a];

        }

    }

2.Berikut adalah kode lengkapnya

#include <iostream>

using namespace std;

int main()

{

    int nilai[5],a,min,max;

    for (a=1;a<=5;a++)

        {

        cout<< "Masukan nilai ke-" << a <<": ";

        cin>> nilai[a];

        }

    min=nilai[1];
    max=nilai[1];
    for(a=2;a<=5;a++)
    {
        if (nilai[a]<min)
        {
            min=nilai[a];
        }
        else if (nilai[a]>max)
        {
            max=nilai[a];
        }
    }
    cout<< "Nilai minimum adalah : "<< min<<endl;
    cout<< "Nilai maximum adalah : "<< max<<endl;

    return 0;
}

3.Berikut adalah flowchartnya

![img](https://raw.githubusercontent.com/amirudin742/Praktikum9/master/Flowchart1.png)

4.Berikut adalah hasilnya

![img](https://raw.githubusercontent.com/amirudin742/Praktikum9/master/Hasil1.png)