#include <stdio.h>
#include <stdlib.h>

void SortFonction(int array[], int size)
{
    int i;
    for (i = 0; i < size; i++)
    {
        int j;
        for (j = 0; j < size; j++)
        {
            if (array[j] > array[j+1])
            {
                int temp = array[j];
                array[j] = array[j+1];
                array[j+1] = temp;
            }
        }
    }
}
void PrintFonction(int array[], int size)
{
    int i;
    for (i = 0; i < size; i++)
    {
        printf("%d  ",array[i]);
    }
}
int EnterFonction(int size)
{
    int array[size], i, c;
    printf("Now Enter some Numbers: ");
    for (i = 0; i < size; i++)
    {
        scanf("%d",&c);
        array[i] = c;
    }
    SortFonction(array, size);
    PrintFonction(array, size);
}

int main()
{
    int size;
    printf("Enter How Much Numbers You want to Enter: ");
    scanf("%d",&size);
    EnterFonction(size);
    return 0;
}
