#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n,m,k;
    scanf("%d %d %d", &n, &m, &k);
    int first[100][100];
    int second[100][100];
    int product[100][100];
    for(int i=0; i<n; i++)
    {
        for(int j=0; j<m; j++)
        {
            scanf("%d", &first[i][j]);
        }
    }

    for(int i=0; i<m; i++)
    {
        for(int j=0; j<k; j++)
        {
            scanf("%d", &second[i][j]);
        }
    }


    for(int i=0; i<n; i++)
    {
        for(int j=0; j<k; j++)
        {
            int sum=0;
            for(int x=0; x<m; x++)
            {
                sum+=first[i][x]*second[x][j];
            }
            product[i][j]=sum;
        }
    }

    for(int i=0; i<n; i++)
    {
        for(int j=0; j<k; j++)
        {
            printf("%d ",product[i][j]);
        }
        printf("\n");
    }
    return 0;
}
