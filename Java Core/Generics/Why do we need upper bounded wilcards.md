Why do we need upper bounded wildcards?
Suppose we have bowl of bananas:

    List<Banana> bananas = new ArrayList<>();
    bananas.add(new Banana());
    bananas.add(new Banana());
    bananas.add(new Banana());
    bananas.add(new Banana());

Then we have a method which received bowl which consist of one particular type of fruit which we don't know:

    public void eatBowlOfAFruit(List<? extends Fruit> fruits) {
        for (Fruit fruit : fruits) {
            fruit.eat(); //we eat a fruit, but we don't know what the fruit is
        }
    }
