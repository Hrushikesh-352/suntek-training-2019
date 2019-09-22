22-sept-assihnment2.txt
#include<stdio.h>
#include<conio.h>
#include<string.h>
int main()
{
    char str1[20], str2[20];
    int len, len1, len2, i, j, found=0, not_found=0;
    printf("Enter first string: ");
    gets(str1);
    printf("Enter second string: ");
    gets(str2);
    len1 = strlen(str1);
    len2 = strlen(str2);
    if(len1 == len2)
    {
        len = len1;
        for(i=0; i<len; i++)
        {
            found = 0;
            for(j=0; j<len; j++)
            {
                if(str1[i] == str2[j])
                {
                    found = 1;
                    break;
                }
            }
            if(found == 0)
            {
                not_found = 1;
                break;
            }
        }
        if(not_found == 1)
            printf("\nStrings are not Anagram");
        else
            printf("\nStrings are Anagram");
    }
    else
        printf("\nBoth string must contain same number of character to be an Anagram Strings");
    getch();
    return 0;
}
=======
 22-sept-assignment3.txt
#include<stdio.h>
#include<string.h>

void main()
{
    int i,j,len,k=0;
    char str[100],rstr[100],vowel[100],consonant[100];
    printf("enter the string:\n");
    gets(str);
    len=strlen(str);
    for(i=0;i<len;i++)
    {
        if(str[i]=='a' || str[i]=='e' || str[i]=='i' || str[i]=='o' || str[i]=='u' )
        {
          vowel[i]=str[i];
        }
        else
        {
         consonant[k]=str[i];
         k++;
        }
    }
    i=1;
    while(str[i]!='\0')
    {
        if(vowel[i]!='a' || vowel[i]!='e' || vowel[i]!='i' || vowel[i]!='o' || vowel[i]!='u')
        {
            rstr[i]=consonant[k];
            k--;
        }
        else
        {
            rstr[i]=vowel[i];
        }
        printf("%c",rstr[i]);
        i++;
    }

=======
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
}
sept-19
