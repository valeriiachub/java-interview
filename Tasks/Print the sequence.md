Print the following sequence without hardcode


    1
    2 1
    1 2 3
    4 3 2 1
    1 2 3 4 5
    6 5 4 3 2 1

**Solution**

    public class SequencePrinter {
        public static void main(String[] args) {
            SequencePrinter sequencePrinter = new SequencePrinter();
            sequencePrinter.printSequence(5);
        }
    
        private void printSequence(int numberOfRows) {
            for(int i = 1; i <= numberOfRows; i++) {
                if(i % 2 != 0) {
                    for(int j = 1; j <= i; j++) {
                        System.out.print(j + " ");
                    }
    
                    System.out.println();
                } else {
                    for(int z = i; z > 0; z--) {
                        System.out.print(z + " ");
                    }
    
                    System.out.println();
                }
            }
        }
    }
