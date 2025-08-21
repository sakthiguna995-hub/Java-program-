# Java-program-
class ArrayHandler {
    private int[] numbers;

    // Constructor to initialize the array
    public ArrayHandler(int size) {
        numbers = new int[size];
        for (int i = 0; i < size; i++) {
            numbers[i] = i * 10; // fill with sample values
        }
    }

    // Method to access array with exception handling
    public void accessElement(int index) {
        try {
            System.out.println("Element at index " + index + " is: " + numbers[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Index " + index + " is out of bounds!");
        }
    }
}

public class ArrayExceptionDemo {
    public static void main(String[] args) {
        ArrayHandler handler = new ArrayHandler(5);

        // Valid access
        handler.accessElement(2);

        // Invalid access (will cause exception)
        handler.accessElement(10);
    }
}