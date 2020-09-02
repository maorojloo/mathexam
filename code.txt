#include <iostream>
#include <time.h>
#include <conio.h>
#include <stdlib.h>
using namespace std;


   int main()
{
srand( time(NULL) );     /// baraye gerftan add random

	int t_soal;
	int s_soal;
	int th_soal=0;
    int t=0;
    int f=0;
    int a;                 ///moteghayer haye barname
	int b;
	int c;
	int javab;
	//---------------------------------------
	cout<<"\t"<<"\t"<<"\t"<<"\t"<<(char)201<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)187<<endl;
	cout<<"\t"<<"\t"<<"\t"<<"\t"<<(char)186<<" math teast!!! "<<(char)186<<endl;                ///titr balaye safhee
	cout<<"\t"<<"\t"<<"\t"<<"\t"<<(char)200<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)205<<(char)188<<endl;
	cout<<"how meny question do you want?";
	for(;;)
	{
		cin>>t_soal;
		if(t_soal<=0) cout<<"please enter number from one!"<<endl;   ///baraye in ke faghat add 1 fi baala ghabol kone
		else break;
	}
cout<<endl;
	cout<<"Select Your ques tion level:"<<endl<<endl;
	cout<<"1-Aval dabestan"<<endl;
	cout<<"2-dovom ta sheshom"<<endl;
	cout<<"3-sheshom bebala"<<endl;
	cout<<"Level ";
	for(;;)
	{
	cin>>s_soal;
	if(s_soal==1||s_soal==2||s_soal==3)             ///baraye inke faghat 1,2,3 ghbolkone
	{
		break;
	}
	else
	{
		cout<<"Pleas select from 1 to tree"<<endl;
	cout<<"Level ";
	}
	}
	///------------------------------------------------------------------------------------------

	for(int x=1;x<=t_soal;x++)                  ///soalat dar in halghe porside mishe (tedad bar asaas vorody kar bar ast)
    {
        cout<<endl;
        th_soal++;
        if (s_soal==1)                         ///Soalat marbot be Aval dabestan
        {


            a=rand()% 9 + 1;///adad aval
            b=rand()% 9 + 1;///adad dovom
            c=rand()% 2 + 1;///noe alamat (+,-)
            if(c==1) ///alamaliyat +
            {
               cout<<th_soal<<"/"<<t_soal<<")"<<a<<"+"<<b<<"=";///soal karbar
               cin>>javab;
               if(javab==a+b)           ///sanjesh soal
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
                   	cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<"false"<<endl;
                   cout<<a<<"+"<<b<<"="<<a+b<<endl;
                   f++;
               }
            }
            //else
              if  (c==2)    ///amaliyat -
            {
                for(;;)
                {
                    if(a<b)         ///bayraye in ke pasokh manfi nashavad
                {
                   a=rand()% 9 + 1;       ///aghar pasokh manfi bod add jadidi tolid konad
                   b=rand()% 9 + 1;
                }
                    else
                        break;
                }
 cout<<th_soal<<"/"<<t_soal<<")"<<a<<"-"<<b<<"=";
               cin>>javab;
               if(javab==a-b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;

               }
               else
               {
                   	cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"-"<<b<<"="<<a-b<<endl;
                   f++;
               }

            }
        }
        else if (s_soal==2)                         ///dovom dabestan ta sheshom
        {
			a=rand()% 99 + 1;
            b=rand()% 99 + 1;
            c=rand()% 4 + 1;
if (c==1)
{
	 cout<<th_soal<<"/"<<t_soal<<")"<<a<<"+"<<b<<"=";
               cin>>javab;
               if(javab==a+b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"+"<<b<<"="<<a+b<<endl;
               }
}
if (c==2)
{
	 cout<<th_soal<<"/"<<t_soal<<")"<<a<<"-"<<b<<"=";
               cin>>javab;
               if(javab==a-b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"-"<<b<<"="<<a-b<<endl;
               }
}
if (c==3)   ///amaliyat x
{
		a=rand()% 30+ 1;
            b=rand()% 30 + 1;

	 cout<<th_soal<<"/"<<t_soal<<")"<<a<<"x"<<b<<"=";
               cin>>javab;
               if(javab==a*b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"x"<<b<<"="<<a*b<<endl;
               }
}
if (c==4)   ///amaliyat ÷
{
	for(;;)
                {
                    if(a%b!=0)    ///baraye inke pasokh baghi mande nadashte bashad
                {
                    a=rand()% 10 + 1;
                    b=rand()% 10 + 1;///tolid add jadid
                }
                    else
                        break;
                }
	 cout<<th_soal<<"/"<<t_soal<<")"<<a<<(char)246<<b<<"=";
               cin>>javab;
               if(javab==a/b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<(char)246<<b<<"="<<a/b<<endl;
               }
				}
                }
        else if (s_soal==3)         ///sateh 3
        {
            a=rand()% 99 + 1;
            b=rand()% 99 + 1;
            c=rand()% 4 + 1;

switch (c)
{
case 1:
 cout<<th_soal<<"/"<<t_soal<<")"<<a<<"+"<<b<<"=";
               cin>>javab;
               if(javab==a+b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"+"<<b<<"="<<a+b<<endl;
               }
break;

case 2:
cout<<th_soal<<"/"<<t_soal<<")"<<a<<"-"<<b<<"=";
               cin>>javab;
               if(javab==a-b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"-"<<b<<"="<<a-b<<endl;
               }
break;

case 3:
a=rand()% 200+ 1;
            b=rand()% 200 + 1;

	 cout<<th_soal<<"/"<<t_soal<<")"<<a<<"x"<<b<<"=";
               cin>>javab;
               if(javab==a*b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<" false "<<endl;
                   cout<<a<<"x"<<b<<"="<<a*b<<endl;
               }
break;

case 4:
   for(;;)
                {
                    if(a%b!=0)
                {
                   a=rand()% 10 + 1;
            b=rand()% 10 + 1;
                }
                    else
                        break;
                }
	 cout<<th_soal<<"/"<<t_soal<<")"<<a<<(char)246<<b<<"=";
               cin>>javab;
               if(javab==a/b)
               {
                   cout<<"\a";///ya (char)7
                   cout<<"ture"<<endl;
                   t++;
               }
               else
               {
               	f++;
               		cout<<"\a"<<"\a"<<"\a";///ya (char)7
                 cout<<"false"<<endl;
                   cout<<a<<(char)246<<b<<"="<<a/b<<endl;
               }
               break;
}
        }
    }
    cout<<endl<<endl<<endl<<endl;
cout<<"true="<<t<<endl;
cout<<"false="<<f<<endl;
cout<<"20/"<<(20/t_soal)*t<<endl;
cout<<"%"<<(100/t_soal)*t<<endl<<endl<<endl<<endl;
cout<<"Enter eny key to exit!" ;
cout<<"by ma.orojloo";
getch();
}



