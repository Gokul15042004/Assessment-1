import java.util.Arrays;
class thirdMax {
    public static void main(String[] args) {
        int a[][]={{5,5,5},{5,5,5},{5,5,5}};
        int max=0;
        int max1=0,max2=0;
        int flag=0;
        int r=a.length;
        int c=a[0].length;
        for(int i=0;i<r;i++){
            for(int j=0;j<c;j++){
                if(max<a[i][j])
                max=a[i][j];
                
                }
            }
            flag=0;
            for(int i=0;i<r;i++){
                for(int j=0;j<c;j++){
                    if((max1<a[i][j])&&(a[i][j]!=max)){
                        max1=a[i][j];
                        
                    }
                }
            }
                flag=0;
                for(int i=0;i<r;i++){
                    for(int j=0;j<c;j++){
                        if((max2<a[i][j])&&(a[i][j]!=max)&&(a[i][j]!=max1)){
                            max2=a[i][j];
                            flag=1;
                        }
                    }
                }
                if (flag==0)
                System.out.println("Array don't have a third max number.");
                else
                System.out.println(max2);
            }
    }
    Output:
    Arrays don't have a third max number.
    

Program 2:
import java.util.*;
class Sort {
    public static void main(String[] args) {
        int[][] a = {
            {5, 4, 7},
            {1, 8, 3},
            {9, 6, 2}};
        int temp[] = new int[9];
        int b = 0;  
        int r = a.length;
        int col = a[0].length;
        for (int[] row : a){
            for (int c : row){
                temp[b++]=c;
            }
        }
        Arrays.sort(temp);
        b=0;
        for (int i=0;i<r;i++){
            for (int j=0;j<col;j++){
                a[i][j]=temp[b++];
            }
        }
        System.out.println("Sorted matrix:");
        for (int[] row:a) {
            for (int c:row) {
                System.out.print(c + " ");
            }
            System.out.println();
        }
    }
}
Output:
1 2 3
4 5 6
7 8 9

Program 3:
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.*;
class  Matrix {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the number of rows and cols: ");
        int r=sc.nextInt();
        int c=sc.nextInt();
        int a[][]=new int[r][c];
        for(int i=0;i<r;i++){
            for(int j=0;j<c;j++)
                a[i][j]=sc.nextInt();
            }
            for(int i=0;i<r;i++){
                for(int j=0;j<c;j++)
                    if((i>=(r/2)-1+i &&j<=(c/2)-1+j));
                    a[j][i] = a[i][j];

                }
               for(int i=0;i<r;i++){
                for(int j=0;j<c;j++) 
                    System.out.print(a[i][j] + "\t");
                    System.out.println();
            }
        }
    }



