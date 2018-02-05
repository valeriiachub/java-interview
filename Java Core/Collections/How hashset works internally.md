## How HashSet works internally?

HashSet uses HashMap internally to store it's objects. 

The elements you add into HashSet are stored as keys of this HashMap object. 
The value associated with those keys will be a constant(`new Object()`). The dummy is used to determine whether or not the element present in the set. For example, `add(E e)` method:

    public boolean add(E e) {
        return map.put(e, PRESENT)==null;
    }

put() method returns previous element stored in the bucket. So if the element is null then there isn't such key and we add the key to set. Otherwise, the key already exists and we don't add the element.