# java

QUESTION 1: 
public class AbnormalConditions {
 public static void main(String[] args) {
 try {
 generateNumberFormatException();
 } catch (NumberFormatException e) {
 System.out.println("Caught NumberFormatException");
 e.printStackTrace();
 }
 try {
 generateStackOverflowError(1);
 } catch (StackOverflowError e) {
 System.out.println("Caught StackOverflowError");
 e.printStackTrace();
 }
 try {
 generateOutOfMemoryError();
 } catch (OutOfMemoryError e) {
 System.out.println("Caught OutOfMemoryError");
 e.printStackTrace();
 }
 }
 private static void generateNumberFormatException() {
 // This will throw NumberFormatException
 String invalidNumber = "abc";
 int number = Integer.parseInt(invalidNumber);
 }
 private static void generateStackOverflowError(int depth) {
 // This recursive call will eventually throw StackOverflowError
 generateStackOverflowError(depth + 1);
 }
 private static void generateOutOfMemoryError() {
 // This will throw OutOfMemoryError
 Object[] array = new Object[1000000];
 for (int i = 0; i < array.length; i++) {
 array[i] = new byte[1024 * 1024]; // 1MB each
 }
 }
}



_____________________

QUESTION 2 :
