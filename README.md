// Maximum-Number-made-out-of-given-number
import java.util.Scanner;
class MaxNum
{
public static void main(String args[])
{
int sum=0,n,i=0,j,t,x=0,c=0,num;

Scanner input=new Scanner(System.in);
System.out.println("enter no. of max 10 digits=");
n=input.nextInt();                       //Input from the user

int[] a=new int[10];             //Array Declaration

num=n;     //Storing value of number entered in another variable to find number of digits

while(num>0)
{
 num=num/10;                //Finding number of digits
 x++;
}

do
{
a[c]=n%10;
n=n/10;
c++;
} while(c<=x);


for(i=0;i<x;i++)
{
for(j=i+1;j<x ;j++)
{
if(a[j]>a[i])
 {
   t=a[i];
   a[i]=a[j];
   a[j]=t;
 }
}
}

for(i=0;i<x;i++)
{
sum=sum*10+a[i];
}
System.out.println("the highest possible no.is="+sum);
}
}
