#include<stdio.h>
#include<stdbool.h>

void Swap(int *x,int *y)
{
    *x = *x + *y;
    *y = *x - *y;
    *x = *x - *y;
}

bool Max(int x,int y)
{
    return x > y;
}

bool Min(int x,int y)
{
    return x < y;
}

//冒泡排序
void BubbleSort(int *p,int n,bool(*q)(int,int))
{
    int temp,swapped;
    for(int i = 0;i < n-1;++i)
    {
        temp = 0;
        for(int j = 0;j < n-i-1;++j)
        {
            if(q(p[j],p[j+1]))
            {
                Swap(&p[j],&p[j+1]);
            }
        }
    }
}
//打印数组
void PrintSort(int arr[],int n)
{
    for(int i = 0;i < n;++i)
    {
        printf("%d ",arr[i]);
    }
}

int main()
{
    int arr[5]={3,5,8,2,6};
    int n = sizeof(arr)/sizeof(arr[0]);
    printf("升序排列：");
    BubbleSort(arr,n,Max);
    PrintSort(arr,n);
    putchar(10);
    printf("降序排列：");
    BubbleSort(arr,n,Min);
    PrintSort(arr,n);
    putchar(10);
    return 0;
}
