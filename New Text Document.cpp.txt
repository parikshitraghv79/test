//Please set the path of the text file before using the program to avoid error
//on the line where comment is set path here. 
#include <string>
using namespace std;
#include <iostream>>
#include<cstdlib>
#include <iomanip>
#include <fstream>
#include<time.h> 


int l = 0; 
int optchoosed [10]; 
void inputs() {cout<<"choose one option from 1 to 4: ";
cin>>optchoosed[l];
l++; ;
  }                                                        //input methd ended



int main() {
	 string answers[30];



srand(time(0));
int arr[31];arr[0]=7;  //array to ensure number dont repeat 
for (int i=1;i<31;i++)
{arr[i]=0;
}
int random[10];
	for(int i=0;i<10;i++)
    {
       int num=rand()%30; //get random number
    num = num+1;
	if (arr[num]==0){
	arr[num]=1;
	   random[i]= num;}
    else{
    	  i--;}
    }
    

      
	int an,bn,cn,dn,en,fn,gn,hn,in,jn;
	an = random[0];
	bn = random[1];
	cn = random[2];
	dn = random[3];
    en = random[4];
	fn = random[5];
	gn = random[6];
	hn = random[7];
	in = random[8];
	jn = random[9];


	
	
	
		string a,b,c,d,e,f,g,h,i,j;
	
	
a = to_string( random[0]	); 
b = to_string( random[1]	);
c = to_string( random[2]	);
d = to_string( random[3]	);
e = to_string(random[4]	);
f = to_string( random[5]	);
g = to_string( random[6]	);
h = to_string( random[7]	);
i = to_string( random[8]	);
j = to_string( random[9]	);

	cout<<"Questions which are asked in this quiz are  "<<endl;
	cout<<a;
	cout<<" ";
	cout<<b;
	cout<<" ";
	cout<<c;
	cout<<" ";
	cout<<d;
	cout<<" ";
	cout<<e;
	cout<<" ";
	cout<<f;
	cout<<" ";
	cout<<g;
	cout<<" ";
	cout<<h;
	cout<<" ";
	cout<<i;
		cout<<" ";
	cout<<j;
	cout<<" "<<'\n'<<endl;


  bool x = false;
	bool y  = false;
	
	// the below code is for reading file
 ifstream inFile;
    string words;
    inFile.open("D:\\test.txt");
     if (!inFile) {
        cout << "Unable to open file";
        exit(1); // terminate with error
    }
    
    
    
     while (inFile >> words) {
    if (words == "ooo"){y = true;
	} 
	if (y==true){
	
    	if (words.compare(a)==0||words.compare(b)==0||words.compare(c)==0||words.compare(d)==0||words.compare(e)==0||words.compare(f)==0||words.compare(g)==0||words.compare(h)==0||words.compare(i)==0||words.compare(j)==0){
    	x = true;}
    if (x==true){
    	if(words == "-") {cout<<'\n';continue;}
    		if(words == "-x-")
	{
	inputs();
	x = false;
	 continue;
	}
    if (x==true){ cout<<words<<" ";}
	
	
                }
	  }
	 
	} 
// the above code is for reading file


int lk=0;
inFile.close();
 inFile.open("D:\\test.txt");// set path here
     if (!inFile) {
        cout << "Unable to open file";
        exit(1); // terminate with error
    }
    
    while (inFile >> words) {
	 if (words=="ooo"){
	 	break;
	 }
	 answers[lk]=words;
	                      lk++;
	 }//while ended - to take correct answer from notepad


int a0 = stoi(answers[an]);
int a1 = stoi(answers[bn]);
int a2 = stoi(answers[cn]);
int a3 = stoi(answers[dn]);
int a4 = stoi(answers[en]);
int a5 = stoi(answers[fn]);
int a6 = stoi(answers[gn]);
int a7 = stoi(answers[hn]);
int a8 = stoi(answers[in]);
int a9 = stoi(answers[jn]);



int score = 0;
if (a0==optchoosed[0]){ score +=1;}
if (a1==optchoosed[1]){ score +=1;}
if (a2==optchoosed[2]){ score +=1;}
if (a3==optchoosed[3]){ score +=1;}
if (a4==optchoosed[4]){ score +=1;}
if (a5==optchoosed[5]){ score +=1;}
if (a6==optchoosed[6]){ score +=1;}
if (a7==optchoosed[7]){ score +=1;}
if (a8==optchoosed[8]){ score +=1;}
if (a9==optchoosed[9]){ score +=1;}

cout<<" Congratulation u completed the quiz and your score is "<<score; 
	
			return 0;

	}//main ended
    	