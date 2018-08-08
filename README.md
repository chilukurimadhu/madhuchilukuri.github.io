# madhuchilukuri.gith

#include <stdio.h>

int main()
{
    char input[100],output[100];
    int i,j=0,n,enckey=0,deckey;
    printf("enter intput data size to encrypt");
    scanf("%d",&n);
    for(i=0;i<=n;i++)
    {
        scanf("%c",&input[i]);
    }
       for(i=0;i<=n;i++)
    {
        output[i]=input[i]+j;
        j++;
    }
       for(i=0;i<=n;i++)
    {
        printf("%c",output[i]);
        enckey=output[i]+enckey;
    }
    //printf("\n%d",enckey);
    printf("if u want to decrypt enter key");
    scanf("%d",&deckey);
    if(deckey==enckey)
    {
        for(i=0;i<=n;i++)
        {
            printf("%c",input[i]);
        }
    }
    else
    {
        printf("wrong key");
    }
    
    return 0;
}
