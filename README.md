# File_Reading_and_Writing_Program


#include <stdlib.h>
#include <stdio.h>
#include <string.h>

int main()
{
	char file_name[100],contents[100];
	
printf("Write the file name with the desired suffix at the end:");
scanf("%s",file_name);
	
FILE *filep = fopen(file_name,"w");
if(filep == NULL)
{
printf("The file could not be written.");
return -1;
}
printf("Write the things you want to write in the file:");
getchar();
fgets(contents, sizeof(contents), stdin);
	
	
int length = strlen(contents);

for(int i = 0;i<length;i++)
{
fputc(contents[i],filep);
printf("%c",contents[i]);
}
fclose(filep);	
return 0;
}
