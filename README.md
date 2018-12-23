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


Latihan2#Menentukan nilai Modus 1.Alur Algoritmanya

	-Membuat fungsi modus dengan void
	-void modus(float bil[],int n,float mod[])
	-mendeklarasikan int n sebagai variabel inputan
	-mendeklarasikan float bil[] sebagai pengingat nilai
	-mendeklrasikan flot mod[] untuk menentukan modus
	-membuat algoritma mengurutkan secara ascending
	-mebuat algoritma untuk menentukan berapa banyak angaka yang muncul
	-membuat algoritma untuk nili yang sering muncul
	-membuat algoritma jika angka sama banyak munculnya

2.Berikut kode lengkaapnya

``#include <iostream>

using namespace std;

int x;

void modus(float bil[],int n,float mod[])

{

int total[100];

int k=1;

x=0;

for(int c=0;c<n;c++)//mengurutkan secara ascending

{

    for(int i=(n-1);i>0;i--)
 
   {

        if (bil[i]<bil[i-1])

        {

            int temp;

            temp=bil[i];

            bil[i]=bil[i-1];

            bil[i-1]=temp;

        }

    }

}

//menghitung berpakali muncul tiap angka

for(int c=0;c<n;c++)

{

    total[c]=0;

    for(int i=0;i<n;i++)

    {

        if(bil[c]==bil[i])

        {

            total[c]++;

        }

    }

}

//Menentukan nilai yang sering muncul

for(int c=0;c<n;c++)

{

    if(total[c]>k)

    {

        k=total[c];

    }

}

//Jika modus lebih dari satu

for(int c=0;c<n;c++)

{

    if(x==0)

        mod[x]=0;

    else

        mod[x]=mod[x-1];

    if(total[c]==k)

    {

        if(bil[c]!= mod[x])

        {

            mod[x]=bil[c];

            x++;

        }

    }

}

//Jika angka muncul sama banyak

int y=0;

for(int c=0;c<n;c++)

{

    if(total[c]==k)

    {

        y++;

    }

}

if(y==n)

{

    x=0;

}

}

int main()

{

    int n;

    float bil[100];
  
    float mod[100];

    cout<<"banyak data :";
    cin>> n;

    for(int c=0;c<n;c++)
    {
        cout<< "Nilai "<<(c+1)<<":";
        cin>> bil[c];
    }
    cout<<endl;
    modus(bil,n,mod);
    if(x==0)
        cout<<"Tidak ada MODUS!"<<endl;
    else
    {
        cout<<"Modus : ";
        for(int c=0;c<x;c++)
        {
            cout<<mod[c]<< "";
        }
    }
}``

3.Berikut adalah hasilnya

![img](https://raw.githubusercontent.com/amirudin742/Praktikum9/master/Hasil2.png)