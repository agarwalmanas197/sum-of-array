# sum-of-array
# WAP that inputs two arrays and saves sum of corresponding elements of these arrays in a third array and prints them.

## For Single Dimension Arrays-

If the size of the array is not same ,then traverse till the size of both the arrays and add them the corresponding elements of both the arrays,then add the remaining elments of the largest array to the end of the sum array.

eg-
" a={1,2,3}
b={1,2}
sum={2,4,3} "

### If size is same

"a={1,2}
b={1,2}
sum={2,4}"

Below is the program for it-

"#include <stdio.h>

int main(void) {
    int N, i;
    scanf("%d", &N);
    // Declare the two arrays
    int numArrayA[N], numArrayB[N], sumArray[N];
    
   // for(i=0;i<N;i++) sumArray[i]=0;
    
    // Get the numArrayA
    for (i=0; i<N; i++) {
        scanf("%d", &numArrayA[i]);
    }
    
    // Get the numArrayB
    for (i=0; i<N; i++) {
        scanf("%d", &numArrayB[i]);
    }
    
    //  logic goes here:
    for(i=0;i<N;i++){
        sumArray[i]=numArrayA[i]+numArrayB[i];
    }
    
    
    // Print the sumArray
    for (i=0; i<N; i++) {
        printf("%d ", sumArray[i]);
    }
    printf("\n");
    return 0;
}"

## For double dimension arrays -

In this program, the user is asked to enter the number of rows r and columns c. Then, the user is asked to enter the elements of the two matrices (of order r*c).


"#include <stdio.h>
int main() {
    int r, c, a[100][100], b[100][100], sum[100][100], i, j;
    printf("Enter the number of rows (between 1 and 100): ");
    scanf("%d", &r);
    printf("Enter the number of columns (between 1 and 100): ");
    scanf("%d", &c);

    printf("\nEnter elements of 1st matrix:\n");
    for (i = 0; i < r; ++i)
        for (j = 0; j < c; ++j) {
            printf("Enter element a%d%d: ", i + 1, j + 1);
            scanf("%d", &a[i][j]);
        }

    printf("Enter elements of 2nd matrix:\n");
    for (i = 0; i < r; ++i)
        for (j = 0; j < c; ++j) {
            printf("Enter element a%d%d: ", i + 1, j + 1);
            scanf("%d", &b[i][j]);
        }

    // adding two matrices
    for (i = 0; i < r; ++i)
        for (j = 0; j < c; ++j) {
            sum[i][j] = a[i][j] + b[i][j];
        }

    // printing the result
    printf("\nSum of two matrices: \n");
    for (i = 0; i < r; ++i)
        for (j = 0; j < c; ++j) {
            printf("%d   ", sum[i][j]);
            if (j == c - 1) {
                printf("\n\n");
            }
        }

    return 0;
}"

### Output-

"Enter the number of rows (between 1 and 100): 2
Enter the number of columns (between 1 and 100): 3

Enter elements of 1st matrix:
Enter element a11: 2
Enter element a12: 3
Enter element a13: 4
Enter element a21: 5
Enter element a22: 2
Enter element a23: 3
Enter elements of 2nd matrix:
Enter element a11: -4
Enter element a12: 5
Enter element a13: 3
Enter element a21: 5
Enter element a22: 6
Enter element a23: 3"

#Sum of two matrices: 
"-2   8   7   

10   8   6"
