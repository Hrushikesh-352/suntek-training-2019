 22-sep-assignment4.txt
/* using iterative method */
#include <stdio.h>
int main()
{
    int n1, n2, i, gcd;
    printf("Enter two integers: ");
    scanf("%d %d", &n1, &n2);
    for(i=1; i <= n1 && i <= n2; ++i)
    {
        // Checks if i is factor of both integers
        if(n1%i==0 && n2%i==0)
            gcd = i;
    }
    printf("G.C.D of %d and %d is %d", n1, n2, gcd);
    return 0;
}

/* using recursive method */

#include <stdio.h>
int main()
{
    int n1, n2;
    
    printf("Enter two positive integers: ");
    scanf("%d %d",&n1,&n2);
    while(n1!=n2)
    {
        if(n1 > n2)
            n1 -= n2;
        else
            n2 -= n1;
    }
    printf("GCD = %d",n1);
    return 0;
=======
#include <stdio.h>
#include <string.h>

int main()
{
   char str[100];
   int c = 0, count[26] = {0}, x;

   printf("Enter a string:\n");
   gets(str);

   while (str[c] != '\0')
   {
   /** Considering characters from 'a' to 'z' only and ignoring others. */

      if (str[c] >= 'a' && str[c] <= 'z')
      {
         x = str[c] - 'a';
         count[x]++;
      }

      c++;
   }

   for (c = 0; c < 26; c++)
   {
   if(count[c]!=0)
      {
       printf("%c - %d \n", c + 'a', count[c]);
      }
   }
   return 0;
}
