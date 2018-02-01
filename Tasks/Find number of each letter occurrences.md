For given 

    String str = "Hello World";
find number of occurrences of each letter.

**Solution**

    public class LetterCounter {
        public static void main(String[] args) {
            LetterCounter letterCounter = new LetterCounter();
    
            String str = "Hello World";
            letterCounter.printLetterOccurrences(str);
        }
    
        public void printLetterOccurrences(String str) {
            char[] chars = str.toCharArray();
    
            Set<Character> uniqueCharacters = new HashSet<>();
            for(Character ch : chars) {
                uniqueCharacters.add(ch);
            }
    
            for(Character ch : uniqueCharacters) {
                if(ch == ' ') {
                    continue;
                }
    
                int numberOfOccurrences = 0;
                for(int i = 0; i < chars.length; i++) {
                    if(chars[i] == ch) {
                        numberOfOccurrences++;
                    }
                }
    
                System.out.println(ch + " - " + numberOfOccurrences);
            }
        }
    }

