# Calculate-S-n-1-x-x-3-3-x-5-5-x-2n-1-2n-1-
Calculate S(n) = 1 + x + x^3/3! + x^5/5! + … + x^(2n+1)/(2n+1)!
#include<stdio.h>
#include<conio.h>
#include<math.h>
int main()
{
int i, n;
float x, S, T;
long M, N;
printf("\nPap x: ");
scanf("%f", &x);
do
{
printf("\nNap n(n >= 1) : ");
scanf("%d", &n);
if(n < 1)
{
printf("\n must be >= 1. Please enter again !");
}

}while(n < 1);

S = 1;
N = 1;
i = 1;

while(i <= n)
{
T = pow(x, (2 * i + 1));
M = i * 2 + 1;
N = N * M * (M - 1);
S = S + x + T/N;
i++;
}
printf("\nTong is %f", S);
getch();
return 0;
}
