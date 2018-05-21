# cw
#include<stdio.h>
#include<time.h>
#include<stdlib.h>
#include <string.h>

int main()
{ 
	FILE *myFileHandle1;
	FILE *myFileHandle2;
	FILE *myFileHandle3;
	FILE *myFileHandle4;
	FILE *myFileHandle5;
	int count = 0;
	char v[1000];
	int row =0;
	int column;
    	char file[100][100];
   	char ch;



	myFileHandle1=fopen("test1.txt", "r");
	myFileHandle2=fopen("test2.txt", "r");
	myFileHandle3=fopen("test3.txt", "r");
	myFileHandle4=fopen("test4.txt", "r");
	myFileHandle5=fopen("test5.txt", "r");

	if(myFileHandle1 != NULL && myFileHandle2 != NULL && myFileHandle3 != NULL && myFileHandle4 != NULL && myFileHandle5 != NULL){
	
		char table[100];

		//initialize
		for(row=0; row<100; row++){
			for(column=0; column<100; column++){
				file[row][column] = 0;
			}
		}
		
		for(row=0; row<100; row++){
			for(column=0; column<100; column++){
				ch  = fgetc(myFileHandle1);
