## Add Cat object to a parameterized list of Dogs

 - You don't have Animal superclass.
 - You can't extend Cat from Dog.


**Solution**

    public class GenericHell {
        public static void main(String[] args) {
            List<Dog> dogs = new ArrayList<>();
            dogs.add(new Dog());
            dogs.add(new Dog());
    
            List dogsAndCats = dogs;
            dogsAndCats.add(new Cat());
            System.out.println(dogs);
        }
    }
    
    class Dog { }
    class Cat { }



