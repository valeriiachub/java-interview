Write a function which will recursively find sum of a list of integers

**Solution**

    public class Solution {
        public static int findSumOfTheListElements(List<Integer> list, int sum, int index) {
            sum += list.get(index);
    
            if(index < list.size() - 1) {
                sum = findSumOfTheListElements(list, sum, ++index);
            }
    
            return sum;
        }
    
        public static void main(String[] args) {
            System.out.println(findSumOfTheListElements(Arrays.asList(1, 2, 3, 4, 5), 0, 0));
        }
    }
