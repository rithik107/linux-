# linux-
to termiate parent and child process

#include<stdio.h>
int main()
{
int pid,status;
pid=fork();
if(pid<0)
{
printf("error");
}
else if(pid==0)
{
printf("child terminating\n");
exit(0);
}
if(wait(&status)!=pid)
printf("wait error\n");
else
printf("parent terminating\n");
}
