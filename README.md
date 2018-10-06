# use-baby-names-
this code to show the babes rank
#include <iostream>
#include<fstream>
using namespace std;

int main()
{
    ifstream file;
    file.open("babynames2012.txt");
    string name;
    cin>>name;
    int ranked=0,check=0;
    string girl,boy;
    while(file>>ranked>>boy>>girl)
    {
        if (name==girl)
        {
            cout<<name<<" is ranked "<<ranked <<" in popularity among girl"<<endl;
            check++;
        }
        if (name==boy)
        {
            cout<<name<<" is ranked "<<ranked <<" in popularity among boy"<<endl;
            check++;
        }
        if (boy ==girl)//
        {
            cout<<name<<" is ranked "<<ranked <<" in popularity among boy&girl"<<endl;
            check++;
        }
    }
    if (check==0)
        cout<<"not found"<<endl;
}
