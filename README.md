# 2162
pbinfo.ro
#include <fstream>
#include <iostream>
using namespace std;

int main()
{
  ifstream inFile;
 inFile.open("conturi.in");
 ofstream outFile;
 outFile.open("conturi.out");
  long long int n,x,a,b,c,cod,i,s;
  inFile>>n>>x;
   s=0; //bankszamla max ereteke
  for(i=1;i<=n;i++)
   inFile>>cod;
   a=cod/100000; //bankszamla szama
   b=cod/10000%10; //nemek (no 2 v ferfi 1)
   c=cod%10000; //bankszamla ertek
     if(a==x && b==2){
       if(c>s)s=c;
   }
   outFile<<s;
}
