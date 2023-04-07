# Matrix-Multiplication
#include <stdio.h>
int main()
{
    int matrix1[10][10], matrix2[10][10], product[10][10];
    int row1, col1, row2, col2, i, j, k;

    printf("enter the number of rows and columns of first matrix:");
    scanf("%d %d", &row1, &col1);

    printf("Enter the elements of first matrix:\n");
    for (i = 0; i < row1; i++)
    {
        for (j = 0; j < col1; j++)
        {
            scanf("%d", &matrix1[i][j]);
        }
    }
    printf("Enter the number of rows and columns in second matrix\n");
    scanf("%d %d", &row2, &col2);

    if (col1 != row2)
    {
        printf(" the matrix can not be multiplied.\n");
        return 0;
    }

    printf(" Enter the elements of second matrix:\n");
    for (i = 0; i < row2; i++)
    {
        for (j = 0; j < col2; j++)
        {
            scanf("%d %d", &matrix2[i][j]);
        }
    }
    for (i = 0; i < row1; i++)
    {
        for (j = 0; j < col2; j++)
        {
            product[i][j] = 0;
            for (k = 0; k < col1; k++)
            {
                product[i][j] += matrix1[i][j] * matrix2[k][j];
            }
        }
    }
    printf("product of the matrices:\n");
    for (i = 0; i < row1; i++)
    {
        for (j = 0; j < col2; j++)
        {
            printf("d% %d", product[i][j]);
        }
        printf("\n");
    }
    return 0;
}
