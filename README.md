public class CircularArrayRotation {
    private int[] rotatedArray;
    
    public CircularArrayRotation(int[] arr, int rotations) {
        int n = arr.length;
        rotatedArray = new int[n];
        
        // Efficient rotation
        rotations %= n;
        
        for (int i = 0; i < n; i++) {
            rotatedArray[(i + rotations) % n] = arr[i];
        }
    }
    
    public int query(int index) {
        return rotatedArray[index];
    }
}
