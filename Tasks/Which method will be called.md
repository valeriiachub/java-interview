## Which method will be called?

    public class Overload{
      public void method(Object o) {
        System.out.println("Object");
      }
      public void method(java.io.FileNotFoundException f) {
        System.out.println("FileNotFoundException");
      }
      public void method(java.io.IOException i) {
        System.out.println("IOException");
      }
      public static void main(String args[]) {
        Overload test = new Overload();
        test.method(null);
      }
    }

You can pass `null` to any method which received reference variable. Compiler will chose narrowest type(`FileNotFoundException` in the case).