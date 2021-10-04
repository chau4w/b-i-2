#include<iostream>
#include<cstring>
#include<string>
using namespace std;
int main()
{
 string array [100]; int size;
	cout << "nhap size ";
	cin >>size;
	cout << "nhap ten cac ban ";
 for (int i=0;i<size;i++) cin >> array[i];
	for (int i=0;i<size-1;i++)
  { int smallest=i;
	   for (int j=i+1;j<size;j++)
						 if (stricmp(array[i],array[j])<0)smallest=j;
    int tam = array[i];
    array[i]=array[smallest];
    array[smallest]=tam;
  }
	 for (int i=0;i<size;i++)
	 cout<<array[i]<<endl;
	return 0;
