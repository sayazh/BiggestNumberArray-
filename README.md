# BiggestNumberArray-
BiggestNumberArray 

import java.util.Scanner;

public class BiggestNumberArray {

	public static void main(String[] args) {

		/*
		 * Given a 2d array of ints, find the biggest number(int) in the array and print
		 * it.
		 */
		Scanner inp = new Scanner(System.in);
		int rows = inp.nextInt(), cols = inp.nextInt();
		int[][] arr = new int[rows][cols];
		for (int i = 0; i <= rows - 1; i++) {
			for (int j = 0; j <= cols - 1; j++) {
				arr[i][j] = inp.nextInt();
			}
		}
		int biggestNumberI = 0;
		int biggestNumberJ = 0;

		for (int i = 0; i <= rows - 1; i++) {
			for (int j = 0; j <= cols - 1; j++) {
				if (arr[i][j] > arr[biggestNumberI][biggestNumberJ]) {
					biggestNumberI = i;
					biggestNumberJ = j;
				}
			}
		}
		System.out.println("The biggest number in 2D array is: ");
		System.out.println(arr[biggestNumberI][biggestNumberJ]);
		inp.close();
	}

}
