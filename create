#include<stdio.h>
#include<conio.h>
int LIS(int arr[],int n)
{
    int lis[n];
    int i,j;
    for(i=0;i<n;i++)
        lis[i]=1;
    for(i=1;i<n;i++)
    {
        for(j=0;j<=i-1;j++)
        {
            if(arr[i]>arr[j])
                lis[i]=max(lis[i],lis[j]+1);
        }
    }
   int m=lis[0];
    for(i=0;i<n;i++)
    {
        if(lis[i]>m)
            m=lis[i];
    }
    return m;
}
int max(int x,int y)
{
    return x>y?x:y;
}
main()
{
    int n,i,res;
    printf("enter the number of elements in the array:\n");
    scanf("%d",&n);
    int arr[n];
    printf("enter the elements:\n");
    for(i=0;i<n;i++)
    {
        printf("enter %d th element:\n",i);
        scanf("%d",&arr[i]);
    }
    res=LIS(arr,n);
    printf("the LIS length is :%d\n",res);
}
