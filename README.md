# what
#include <iostream>
#include <ctime>
using namespace std;
int add(int a, int b){
    return a+b;

}
int sub(int a, int b){
    return a-b;

}
int multiply(int a,int b){
    return a*b;
}
char menu(){
    char choice;
    cout <<"1)add two number\n";
    cout<<"2)sub two number\n";
    cout <<"3)multiply two number\n";
    cout<<"0)quit\n";
    cout<<"enter your choice\n";
    cin>>choice;
    return choice;
}
bool answerQueation(int num1,int num2,int (*f)(int,int),int answer){
    return f(num1,num2)==answer;
}
int main(){
    srand((unsigned)time(NULL));
    while(true){
        char choice=menu();
        if (choice=='0')
            break;
        int num1,num2;
        num1=rand()%90+10;
        num2=rand()%90+10;

decltype(add)*pf;
char op;
switch(choice){
case '1':pf=add;op='+';break;
    case '2':pf=sub;op='-';break;
case'3':pf=multiply;op='*';break;
default:continue;
}
int answer;
cout<<num1<<op<<num2<<"=?";
cin>>answer;
if(answerQueation(num1,num2,pf,answer)==true)
    cout<<"Correct!"<<endl;
else
    cout<<"Wrong!"<<endl;
    }return 0;
}
