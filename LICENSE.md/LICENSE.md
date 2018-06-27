#include<iostream>
#include <string>  
#include <vector>  
#include <fstream>  
#include <sstream> 
using namespace std;


struct actor{
	string name;
	string sex;
	string program_name;
	string program_type;
	string class_number;
	string phone_number;
}; 

struct referee{
	string name;
	string sex;
	double score[5];
}; 

void read()
{
	// 读文件  
    ifstream inFile("data.csv", ios::in);  
    string lineStr;  
    vector<vector<string> > strArray;  
    while (getline(inFile, lineStr))  
    {  
        // 打印整行字符串  
        cout << lineStr << endl;  
        // 存成二维表结构  
        stringstream ss(lineStr);  
        string str;  
        vector<string> lineArray;  
        // 按照逗号分隔  
        while (getline(ss, str, ','))  
            lineArray.push_back(str);  
        strArray.push_back(lineArray);  
    }    
    getchar();
}

int main()
{
	struct actor a[5];
	struct referee r[5];
	FILE *file = fopen("data.csv" , "r");//第一个参数传入你的路径，也即"路径/*.csv"
	
	
	
	read();
	return 0;	
}
	
