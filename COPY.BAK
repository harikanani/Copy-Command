//copy src.txt dest.txt
//wap prg to copy two files

#include<iostream.h>
#include<conio.h>
#include<fstream.h>
#include<stdlib.h>
#include<string.h>
void main(int n,char *data[])
{
	ifstream fin;
	ofstream fout;
	char ch;

	cout<<"For more information on a specific command, type --help Command-name"<<endl;

	if(n==2 && strcmp(data[1],"--help")==0)
	{
		cout<<"------------ HELP -------------"<<endl;
		cout<<"Documentation of Copy Command Created By Harikrushn Kanani.";
		cout<<endl;
		cout<<"Commands: "<<endl<<endl;
		cout<<"--help    : To get Help Menu."<<endl;
		cout<<"--version : To get the Version of the Software."<<endl;
		cout<<"--formate : To get the Formate of the Command."<<endl;
	}
	else if(n==2 && strcmp(data[1],"--version")==0)
	{
		cout<<"Copy Command."<<endl;
		cout<<"Version V1.0"<<endl;
	}
	else if(n==2 && strcmp(data[1],"--formate")==0)
	{
		cout<<"Formate : copy [source file name] [destination file name]";
		cout<<endl;
	}
	else if(n<=1)
	{
		cout<<"Insufficient Number of Arguments."<<endl;
		cout<<"Please Provide Source File and Destination File names."<<endl;
		cout<<"Formate : copy [source file name] [destination file name]";
		cout<<endl;
	}
	else if(n<=2)
	{
		cout<<"Insufficient Number of Arguments."<<endl;
		cout<<"Please Provide Destination File name."<<endl;
		cout<<"Formate : copy [source file name] [destination file name]";
		cout<<endl;
	}
	else
	{
		fin.open(data[1]);
		if(!fin.good())
		{
			cout<<data[1]<<" File Doesn't Exists."<<endl;
			cout<<"Please Enter Existing Source File name."<<endl;
		}
		else
		{
			for(int i=1; i<n-1; i++)
			{
				fout.open(data[i+1]);
				fin.get(ch);
				while(!fin.eof())
				{
					fout<<ch;
					fin.get(ch);
				}
				cout<<data[1]<<" file copied into "<<data[i+1]<<" File."<<endl;
				fout.close();
//				fin.seekg(0,ios::beg);
				fin.close();
				fin.open(data[1]);
			}
		}
	}
	fin.close();
	getch();
}
/*   ---------------------------------------------------------------------
				First i have implement this after this i have
				implemented the functionality in this and make it good.
	 ---------------------------------------------------------------------


	for(int i=1; i<n; i++)
	{
		fin.open(data[0],ios::in);
		if(!fin.good())
		{
			cout<<data[0]<<" File doesn't Exists."<<endl;
		}
		else	//	File is Exists.
		{
			fout.open(data[i+1]);
			fin.get(ch);
			while(!fin.eof())
			{
				fout<<ch;
				fin.get(ch);
			}
			cout<<data[i]<<" File is Copied into "<<data[i+1]<<endl;
			fout.close();
		}
	}
	fin.close();
*/
