# c--programming-p10
p10 c++
/* WACP to remove duplicate elements iin a single dimensional array */
#include<stdio.h>
int main()
{
    int a[50],i,j,k,dup[50],number;
    printf("enter size of the array:");
    scanf("%d",&number);
    printf("enter elements of the array:");
    for(i=0;i<number;i++)
        {
            scanf("%d",&a[i]);
            dup[i]=-1;
        }
    printf("entered elements are:");
    for(i=0;i<number;i++)
        {
            printf("%d\t",a[i]);
        }
    for(i=0;i<number;i++)
        {
            for(j=i+1;j<number;j++)
                {
                    if(a[i]==a[j])
                    {
                        for(k=j;k<number;k++)
                            {
                                a[k]=a[k+1];
                            }
                        j--;
                        number--;
                    }
                }
        }
    printf("\n after deleting the duplicate element the array is:");
    for(i=0;i<number;i++)
        {
            printf("%d\t",a[i]);
        }
    return 0;
}

output:
enter size of the array:6
enter elements of the array:8
9
9
8
5
4
entered elements are:8	9	9	8	5	4	
 after deleting the duplicate element the array is:8	9	5	4	
