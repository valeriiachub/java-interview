## How to generate a stream?
There are two ways to generate a stream:
1. Use Stream#generate(Supplier) method:
    Random random = new Random();  
    Stream.generate(random::nextInt).limit(100).forEach(System.out::println);
2. Use Stream#iterate(final T seed, final UnaryOperator<T> f)
UnaryOperator is used to determine how the new element will be calculated based on previous element.

