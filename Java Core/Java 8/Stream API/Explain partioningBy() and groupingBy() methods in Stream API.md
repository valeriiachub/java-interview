Explain groupingBy() and partitioningBy() methods in Stream API?
Both methods groups stream entries. The only difference between them is that partioningBy groups by booleans and groupingBy() groups by boolean and any other Object.

Example:

    public class Demo {
        public static void main(String[] args) {
            Person p1 = new Person("Kosa", 21);
            Person p2 = new Person("Saosa", 21);
            Person p3 = new Person("Tiuosa", 22);
            Person p4 = new Person("Komani", 22);
            Person p5 = new Person("Kannin", 25);
            Person p6 = new Person("Kannin", 25);
            Person p7 = new Person("Tiuosa", 22);
            ArrayList<Person> list = new ArrayList<>();
            list.add(p1);
            list.add(p2);
            list.add(p3);
            list.add(p4);
            list.add(p5);
            list.add(p6);
            list.add(p7);
    
            // groupingBy
            Map<Object, List<Person>> list2; list2 = list.stream().
                    collect(Collectors.groupingBy(p -> p.toString()));
            System.out.println("grouping by age -> " + list2);
    
            // partitioningBy
            Map<Boolean, List<Person>> list3 = list.stream().
                    collect(Collectors.partitioningBy(p -> p.getAge() == 22));
            System.out.println("partitioning by age -> " + list3);
        }
    }
    
    class Person {
        String name;
        int age;
    
        Person(String name, int age) {
            this.name = name;
            this.age = age;
        }
    
        public String getName() {
            return name;
        }
    
        public int getAge() {
            return age;
        }
    
        public String toString() {
            return this.name;
        }
    }

