#include <iostream>
#include <fstream>
using namespace std;

//Struct student with their name, age, and grade.
struct student{
	char firstName[10];
	char lastName[15];
	int age;
	float grade;
};

//Function prototypes
void readData(student values[10]);
void findHighestGrade(student values[10]);
void findLowestGrade(student values[10]);
float findAvgGrade(student values[10]);


int main(){
	//Array of the struct values.
	student values[10];

	//Function calls.
	readData(values);
	findHighestGrade(values);
	findLowestGrade(values);

	//Calls the function and prints results.
	float avgGrade;
	avgGrade = findAvgGrade(values);
	cout << "Class Average:\t" << avgGrade << endl;

	return 0;
}

//Reads in data from students file and puts in struct.
void readData(student values[]){
	//Creates input stream variable.
	ifstream fin;
	fin.open("students");
	//Puts information from file into struct.
	for(int i = 0; i < 10; i++){
		fin >> values[i].firstName;
		fin >> values[i].lastName;
		fin >> values[i].age;
		fin >> values[i].grade;
	}
	fin.close();
}

//Finds the highest grade and prints all info with it.
void findHighestGrade(student values[]){
	//Variable to follow what "i" is in order to print all info later.	
	int index;
	//Sets the first grade to be the max to start with.
	float max = values[0].grade;
	for(int i = 0; i < 10; i++){
		if(values[i].grade > max){
			max = values[i].grade;
			index = i;
		}
	}
	cout << "Highest Grade:  ";
	cout << values[index].firstName << "  ";
	cout << values[index].lastName << "  ";
	cout << values[index].age << "  ";
	cout << values[index].grade << "  " << endl;
}

//Finds the lowest grade and prints all info with it.
void findLowestGrade(student values[]){
	//Variable to follow what "i" is in order to print all info later.		
	int index;
	//Sets the first grade to be the min to start with.
	float min = values[0].grade;
	for(int i = 0; i < 10; i++){
		if(values[i].grade < min){
			min = values[i].grade;
			index = i;
		}
	}
	cout << "Lowest Grade:  ";
	cout << values[index].firstName << "  ";
	cout << values[index].lastName << "  ";
	cout << values[index].age << "  ";
	cout << values[index].grade << "  " << endl;

}

float findAvgGrade(student values[10]){
	//Start sum and avg to be 0.
	float sum = 0;
	float avg = 0.000;
	for (int i = 0; i < 10; i++){
		sum = sum + values[i].grade;
	}
	avg = sum / 10.000;

	return avg;
}
