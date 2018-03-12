## Why do we need init() methods in our beans?  
The first step of bean instantiation is to create object via constructor. But what if we need to access something Spring configures in our constructor? Lets say we have annotation which inject some random value in our field. How we can access in constructor? 

For the purpose we have init() method which will be called after constructor but before placing the bean in the container.
