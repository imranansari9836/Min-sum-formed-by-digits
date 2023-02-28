class Solution {
    
    public static long minSum(int arr[], int n)
    {
     Arrays.sort(arr);
 
        // let two numbers be a and b
        long a = 0, b = 0;
        for (int i = 0; i < n; i++) {
 
            // fill a and b with every alternate
            // digit of input array
            if (i % 2 == 0)
                a = a * 10 + arr[i];
            else
                b = b * 10 + arr[i];
        }
 
        // return the sum
        return a + b;
    }
}
