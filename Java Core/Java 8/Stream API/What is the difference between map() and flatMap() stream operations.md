## What is the difference between map() and flatMap() stream operations?
-   The function you pass to map() operation returns a single value.
-   The function you pass to flatMap() opeartion returns a Stream of value.
-   flatMap() is combination of map and flat operation.
-   map() is used for transformation only, but flatMap() is used for both transformation and flattening.

The flatMap() can be used in the situation when we have two-level data structure(for example, list of lists) and we want to obtain all the elements into single stream.
Example:

    public class Demo {
        public static void main(String[] args) {
            int[][] multi = new int[][]{
                    {1, 2, 3, 4},
                    {4, 3, 2, 1},
                    {5, 6, 7, 8},
                    {8, 7, 6, 5},
            };
    
            List<Integer> collect = Arrays.stream(multi).flatMapToInt(Arrays::stream).boxed().collect(Collectors.toList());
            System.out.println(collect);
        }
    }
