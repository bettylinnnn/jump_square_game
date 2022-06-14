#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#include<conio.h>
#include <unistd.h>
#include<iostream>
#include<windows.h>
 
 
int gotoxy(int,int);//清除用 
int color(int );	//改顏色 
int first();	//剛開始的遊戲介紹介面 
int main(){
	srand((unsigned) time(NULL) + getpid());	//產生亂數 
	char array[20][100]={0},a;	//陣列 
	int block[4];		//上到下有有四格，上到下是0,1,2,3 
	int random_n=4,n,i,j;
	int ch;
	int enter_to_start;
	int choose_color;	//按鍵接收到的 
	int which_color=0;	//陣列裡面的第幾個 
	int color_blank[10]={0xff,0x88,0x11,0x22,0x33,0xee,0xdd,0x99,0xaa,0xcc};	//方塊顏色色號 
	int color_word[10]={0x0f,0x0b,0x01,0x02,0x03,0x0e,0x0d,0x09,0x0a,0x0c};		//剛開始的字顏色 
	int score=0;	//計分 
	int again;		//還要不要玩 
	int highest_score=0;	//紀錄最高分 


    
 	for(i=0;i<30;i++){		//畫框框 
			for(j=0;j<115;j++){
				if(i==0||i==29){printf("-");
				}
				else if(j==0||j==114)printf("|");
				else printf(" ");
		}printf("\n");
	}
	
	for(i = 0; i < 10; i++)   //讓字一直改變顏色 
    {
        gotoxy(0,0);	//從(0,0)的位置開始覆印
        printf("\n\t\t");
        color(color_word[i]);
        printf("我有一個冰淇淋\n");
        color(07);
        _sleep(350);	//停0.35秒 
    }
   	char word1[]="歡迎來到:杯體的跳格子遊戲\n";
   	char word2[]="|\t\t\t\t 利用方向鍵(←↓→)\n\t\t\t\t 當最下面哪個格子亮\n\t\t\t\t 就按哪個\n\n";
   	char word3[]="|方向鍵左右選擇格子的顏色(好了按Enter):\t";
   	printf("| ");
	for(i =0;word1[i]!='\0';i++)//只要後面的字不是空的，就讓字一個一個出現 
    {
        printf("%c",word1[i]);
        Sleep(159);
    }
    for(i =0;word2[i]!='\0';i++)
    {
        printf("%c",word2[i]);
        Sleep(87);
    }
    for(i =0;word3[i]!='\0';i++)
    {
        printf("%c",word3[i]);
        Sleep(150);
    }
    

    Sleep(987);	
	
	while(1)	//讓遊戲可以玩無限多次 
	{score=0;	//讓分數歸零 
		system("cls");	//清空畫面 
		
		first();
	color(color_blank[which_color]);
				printf("hello world");
				color(07);		//顏色要改回來 不然之後的顏色都會跟前面長一樣 
	
	while(choose_color=getch())		//接收控制鍵 
	{				
		if(choose_color==77)		//當按下右鍵 
		{
			which_color++;

			if(which_color>9)		//因為我的顏色陣列只有十個，第十個還要右鍵就從零開始 
			{
				which_color=0;
				system("cls");		//清版面  
				first();
				color(color_blank[which_color]);	//改成下一個的顏色 
				printf("hello world");	//我只是要印出長長的長方型(隨便打 
				color(07);//顏色印完顏色要改回來 
			}
			else
			{
				system("cls");		//清版面 			
				first();
				color(color_blank[which_color]);	//改成下一個的顏色
				printf("hello world");
				color(07);
			}
			
			
		
		
		}
		else if(choose_color==75)		//當我按下左鍵 
		{
			which_color--;		//陣列減一 
			if(which_color<0)	//因為顏色只有十種 
			{
				which_color=9;	//0的話要跳到第10個顏色 
				system("cls");
				first();
				color(color_blank[which_color]);	//顏色改成我要的顏色 
				printf("hello world");
				color(07);
			}
			else
			{
					system("cls");
				first();
				color(color_blank[which_color]);
				printf("hello world");
				color(07);
			}
		
			
		}
		else if(choose_color==13) break;	//按enter的時候，跳出來 
	}
	
	system("cls");		//清版面 
for(i=0;i<20;i++){		//設置陣列 
		for(j=0;j<100;j++){
			array[i][j]=' ';//每個陣列都是空白 
		}
	}
	//i=0~4 block[0]
	//i=5~9 block[1]
	//i=10~14 block[2]
	//i=15~19 block[3]
	//j=15~24  1
	//j=25~34  2
	//j=35~44  3
	
	
	while(random_n-->0){		//1~3取亂數 
		n=6 * rand() / RAND_MAX + 1;	//因為怕亂數不平均 用1~6 
		if(n>3)block[random_n]=n-3;		//如果大於3就-3，這樣就是1~3的數字了 
		else block[random_n]=n;
	}
	
	if(block[0]==1){		//最上面那個格子是1的話(詳見圖表) 
	
		for(i=0;i<5;i++){		 
		for(j=15;j<24;j++){		
			array[i][j]='5';	//顯示我要的方塊為5 
		}}}
		else if(block[0]==2){
			for(i=0;i<5;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
		
			for(i=0;i<5;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[1]==1){
	
		for(i=5;i<10;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[1]==2){
			for(i=5;i<10;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
			for(i=5;i<10;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[2]==1){
	
		for(i=10;i<15;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[2]==2){
			for(i=10;i<15;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[2]=3){
			for(i=10;i<15;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[3]==1){
	
		for(i=15;i<20;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[3]==2){
			for(i=15;i<20;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[3]=3){
			for(i=15;i<20;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}	}
	for(i=0,j=14;i<20;i++){		//設定我的分隔線為1 
		
		array[i][j]='1';
		
	} 
	for(i=0,j=44;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=24;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=34;i<20;i++){
		
		array[i][j]='1';
		
	} 


printf("分數:%d\n",score);
for(i=0;i<20;i++){
	
		for(j=0;j<100;j++){		//最開始要先顯示格子 
			if(array[i][j]=='5'){//遇到格子改顏色 
				color(color_blank[which_color]);
				printf("%c",array[i][j]);
				color(07);
			}
			else if(array[i][j]=='1'){//遇到1改顏色 
				color(0x77);
				printf("%c",array[i][j]);
				color(07);
			}
			else
			printf(" "); //都不是就印空格 
			
		}printf("\n");
	}
	
	
		while(ch=getch()){
		if(ch==77&&block[3]==3){		//按下右鍵而且最下面的格子也在最右邊的時候 
			score ++;
			block[3]=block[2];	//格子往下移 
			block[2]=block[1];
			block[1]=block[0];
			n=6 * rand() / RAND_MAX + 1;	//因為怕亂數不平均 用6去除 
		if(n>3)block[0]=n-3;
		else block[0]=n;		//原本的格子下移，最上面的格子隨機找 
		
for(i=0;i<20;i++){
		for(j=0;j<100;j++){	
			array[i][j]=' ';		//將所有的格子先歸零，不然印出來會把上次的格子也都印出來 	
		}
	}
		if(block[0]==1){		//設定新的格子 
	
		for(i=0;i<5;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[0]==2){
			for(i=0;i<5;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
		
			for(i=0;i<5;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[1]==1){
	
		for(i=5;i<10;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[1]==2){
			for(i=5;i<10;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
			for(i=5;i<10;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[2]==1){
	
		for(i=10;i<15;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[2]==2){
			for(i=10;i<15;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[2]=3){
			for(i=10;i<15;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[3]==1){
	
		for(i=15;i<20;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[3]==2){
			for(i=15;i<20;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[3]=3){
			for(i=15;i<20;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}	}
		gotoxy(0,0);	//從(0,0)的位置開始印	
		//這邊不用system("cls")是因為這個方法是把所有印出的東西清掉
		//快速的話螢幕會一直閃。這裡使用從零開始印去覆蓋，就不太會有這個問題 
		for(i=0,j=14;i<20;i++){
			array[i][j]='1';	//設定直線 
		} 
	for(i=0,j=44;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=24;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=34;i<20;i++){
		
		array[i][j]='1';
		
	} 
		printf("分數:%d\n",score);
		
		for(i=0;i<20;i++)		//印出格子 
		{
		for(j=0;j<100;j++)
		{
			if(array[i][j]=='5'){
				color(color_blank[which_color]);
				printf("%c",array[i][j]);
				color(07);
			}
			else if(array[i][j]=='1'){
				color(0x77);
				printf("%c",array[i][j]);
				color(07);
			}
			else
			printf("%c",array[i][j]);
			
		}printf("\n");
		}
		
	
		}
		else if(ch==80&&block[3]==2)		//下鍵 
		{	
			score ++;
			block[3]=block[2];
			block[2]=block[1];
			block[1]=block[0];
			n=6 * rand() / RAND_MAX + 1;	//因為怕亂數不平均 用6去除 
		if(n>3)block[0]=n-3;
		else block[0]=n;
		for(i=0;i<20;i++){
		for(j=0;j<100;j++){
			
			array[i][j]=' ';
			
		}
	}

		if(block[0]==1){
	
		for(i=0;i<5;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[0]==2){
			for(i=0;i<5;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
		
			for(i=0;i<5;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[1]==1){
	
		for(i=5;i<10;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[1]==2){
			for(i=5;i<10;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
			for(i=5;i<10;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[2]==1){
	
		for(i=10;i<15;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[2]==2){
			for(i=10;i<15;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[2]=3){
			for(i=10;i<15;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[3]==1){
	
		for(i=15;i<20;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[3]==2){
			for(i=15;i<20;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[3]=3){
			for(i=15;i<20;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}	}
		gotoxy(0,0);
			for(i=0,j=14;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=44;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=24;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=34;i<20;i++){
		
		array[i][j]='1';
		
	} 

		printf("分數:%d\n",score);
		
		for(i=0;i<20;i++)
		{
		for(j=0;j<100;j++)
		{
		if(array[i][j]=='5'){
				color(color_blank[which_color]);
				printf("%c",array[i][j]);
				color(07);
			}
			else if(array[i][j]=='1'){
				color(0x77);
				printf("%c",array[i][j]);
				color(07);
			}
			else
			printf("%c",array[i][j]);
			
		}printf("\n");
		}
		
		}
		else if(ch==75&&block[3]==1)		//左鍵
		{
			score ++;
			block[3]=block[2];
			block[2]=block[1];
			block[1]=block[0];
			n=6 * rand() / RAND_MAX + 1;	//因為怕亂數不平均 用6去除 
		if(n>3)block[0]=n-3;
		else block[0]=n;
		for(i=0;i<20;i++){
		for(j=0;j<100;j++){
			array[i][j]=' ';
			
		}
	}

		if(block[0]==1){
	
		for(i=0;i<5;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[0]==2){
			for(i=0;i<5;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
		
			for(i=0;i<5;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[1]==1){
	
		for(i=5;i<10;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[1]==2){
			for(i=5;i<10;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else {
			for(i=5;i<10;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[2]==1){
	
		for(i=10;i<15;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[2]==2){
			for(i=10;i<15;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[2]=3){
			for(i=10;i<15;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}}
		
	if(block[3]==1){
	
		for(i=15;i<20;i++){
		for(j=15;j<24;j++){
			array[i][j]='5';
		}}}
		else if(block[3]==2){
			for(i=15;i<20;i++){
		for(j=25;j<34;j++){
			array[i][j]='5';
		}
		}}
		else if(block[3]=3){
			for(i=15;i<20;i++){
		for(j=35;j<44;j++){
			array[i][j]='5';
		}
		}	}
		gotoxy(0,0);
			for(i=0,j=14;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=44;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=24;i<20;i++){
		
		array[i][j]='1';
		
	} 
	for(i=0,j=34;i<20;i++){
		
		array[i][j]='1';
		
	} 

printf("分數:%d\n",score);
		for(i=0;i<20;i++)
		{
		for(j=0;j<100;j++)
		{
			if(array[i][j]=='5'){
				color(color_blank[which_color]);
				printf("%c",array[i][j]);
				color(07);
			}
			else if(array[i][j]=='1'){
				color(0x77);
				printf("%c",array[i][j]);
				color(07);
			}
			else
			printf("%c",array[i][j]);
			
		}printf("\n");
		}
		
		}
		else if(ch==77&&block[3]!=3)	//如果最下面顯示右邊但是按錯的話 
		{
		break;	//跳出來 
			
			
		}
		else if(ch==80&&block[3]!=2)	//如果最下面顯示中間但是按錯的話 
		{
			break;
		}
		else if(ch==75&&block[3]!=1)	//如果最下面顯示但是左邊按錯的話 
		{
			break;
		}
		

		
	}
	if(score>highest_score){
		highest_score=score;//如果分數高於最高分，設成最高分 
	}
	
	system("cls");
	printf("\n\n\n\t\t\t!!恭喜你獲得%d分!!!!\n",score);
	if(highest_score==score)//最高分的話 顯示 
	{
		printf("\n\n\n\t\t\t\t恭喜你創下大會紀錄");
	}
	printf("\n\n\n\t\t\t歷史最高分:%d\n",highest_score);
	if(highest_score>score)	printf("\n\n\t\t\t快來破紀錄吧!"); 
	printf("\n\n\t\t\t還要玩嗎?(y/n)");
	while(again=getch())
	{
		if(again=='y')		//如果打y 
	{
		break;		//跳出去 回到最前面的while(1) 
	}
	else if(again=='n')
	return 0;		//不要的話就停止 
	}
	
	}
}

int gotoxy(int xpos, int ypos)//先把游標用 gotoxy() 移到最開始的地方，因為我要覆蓋的東西位置都一樣
{								//，移回到一開始的地方直接重印 
  COORD scrn;
  HANDLE hOuput = GetStdHandle(STD_OUTPUT_HANDLE);
  scrn.X = xpos; scrn.Y = ypos;
  SetConsoleCursorPosition(hOuput,scrn);
}
int color(int c)
{
    SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), c); //顏色設置
    //SetConsoleTextAttribute是一個API(應用程序編成接口) 
}
int first()
{
	printf("\n\n");
	printf("歡迎來到:杯體的跳格子遊戲\n");
	printf("\t\t\t 利用方向鍵(←↓→)\n");
	printf("\t\t\t 當最下面哪個格子亮\n");
	printf("\t\t\t 就按哪個\n\n");
	printf("方向鍵左右選擇格子的顏色(好了按Enter):\t");

}
