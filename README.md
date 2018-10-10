# StructExc3Apteka
Да се напише програма, която създава структура Apteka с полета name, mg, number, и price, указващи наименованието, милиграмите, количеството опаковки и цена на лекарствта. Да се въведе цяло число n и след него n на брой данни за лекарствени препарати.Г) Да се намери броя на лекарствата с цена между 10 и 50 лева.

#include<iostream>
#include<cstring>
#include <iomanip>
using namespace std;
struct Apteka
{
    string name;
    float mg;
    int number;
    double price;
};
int main()
{
    int n;
    cout<<"Number of medicines: ";
    cin>>n;
    Apteka medicine[n];
    for(int i=0;i<n;i++)
    {
        cout<<"*****Medicine*****"<<i+1<<endl;
        cout<<"Name: ";
        cin.get();
        cin>>medicine[i].name;
        cout<<"Mg: ";
        cin.get();
        cin>>medicine[i].mg;
        cout<<"Number: ";
        cin>>medicine[i].number;
        cout<<"Price: ";
        cin>>medicine[i].price;
    }
    cout<<"Number of medicines with price between 10 and 50: "<<endl;
    int count =0;
    for(int i=0;i<n;i++)
    {
              if(medicine[i].price>10 && medicine[i].price<50)
            {
                 count++;
            }
       
    }
    cout<<count<<endl;;
    
    system("pause");
    return 0;
}
