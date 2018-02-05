## Explain reference variable and instance variable type parameters
**Reference variable type parameter** adds type checking while working with the list after initialization.

    List<Dog> dogs = ...
    //Now we can add only dogs to the list.


----------


Although, we can omit **instance variable type parameter** for the list and suddenly in the list of dogs we have cats:

    List<Cat> cats = new ArrayList<>();
    List<Dog> dogs = new ArrayList(cats);

So, **instance variable type parameter** is responsible for not allowing wrong type of objects to be passed at the list construction time.