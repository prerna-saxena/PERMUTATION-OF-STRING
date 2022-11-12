# PERMUTATION-OF-STRING


#include <stdio.h>
#include <conio.h>
#include <stdlib.h>

void permute(char *a, int n, int l, int r)
{
    int i;
    if(l==r)
    {
        printf("%s\n", a);
    }
    else
    {
        for(i=l;i<=r; i++)
        {
            swap((a+l), (a+i));
            permute(a, l+1, r);
            swap((a+l), (a+i));
        }
    }
}
 
