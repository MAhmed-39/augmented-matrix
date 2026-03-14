public class Main {
    public static void main (String[]args) {
        
        double[][] A = {{1, 2, 3} , {4, 5, 6}};
        
        int row = A.length;
        int col = A[0].length;
        
        for (int i=0 ; i < row ; i++)
        {
            double a = A[i][i];
            
            for (int j=0 ; j < col ; j++)
            {
                A[i][j] /= a;
            }
            
            for (int k=0 ; k < row ; k++)
            {
                if (i != k)
                {
                    double b = A[k][i];
                    for (int l=0 ; l < col ; l ++)
                    {
                     A[k][l] = A[k][l] - (b*A[i][l]);
                    }
                }
            }
            
        }
        
        for (int m=0 ; m < row ; m++)
        {
            for (int n=0 ; n < col ; n++)
            {
                System.out.print(A[m][n]+ "    ");
            }
            
            System.out.println();
        }
    }
}
