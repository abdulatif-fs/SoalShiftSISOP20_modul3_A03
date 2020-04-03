# SoalShiftSISOP20_modul3_A03
Batu mulia pertama. Emerald. Batu mulia yang berwarna hijau mengkilat. Pada
batu itu Ia menemukan sebuah kalimat petunjuk. Ada sebuah teka-teki yang berisi:
1. Buatlah program C dengan nama "4a.c", yang berisi program untuk
melakukan perkalian matriks. Ukuran matriks pertama adalah 4x2, dan
matriks kedua 2x5. Isi dari matriks didefinisikan di dalam kodingan. Matriks
nantinya akan berisi angka 1-20 (tidak perlu dibuat filter angka).
2. Tampilkan matriks hasil perkalian tadi ke layar.


  #include <stdio.h>
#define N 5
void multiply(int mat1[][N], int mat2[][N], int res[][N]) 
{ 
    int i, j, k; 
    for (i = 0; i < N; i++) 
    { 
        for (j = 0; j < N; j++) 
        { 
            res[i][j] = 0; 
            for (k = 0; k < N; k++) 
                res[i][j] += mat1[i][k]*mat2[k][j]; 
        } 
    } 
} 
  
int main() 
{ 
    int mat1[N][N] = { {1, 2}, 
                    {3, 4}, 
                    {5, 6}, 
                    {7, 8}}; 
  
    int mat2[N][N] = { {1, 2, 3, 4, 5}, 
                    {6, 7, 8, 9, 10}}; 
  
    int res[N][N]; // To store result 
    int i, j; 
    multiply(mat1, mat2, res); 
    for (i = 0; i < N; i++) 
    { 
        for (j = 0; j < N; j++) 
           printf("%d ", res[i][j]); 
        printf("\n"); 
    } 
  
    return 0; 
} 
