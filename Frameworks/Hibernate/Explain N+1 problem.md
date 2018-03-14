## Explain N+1 problem
The N+1 SELECT problem is a result of lazy loading and load on demand fetching strategy. In this case, Hibernate ends up executing N+1 queries to populate a collection of N elements. 

For example, if you have a List of N Items where each Item has a dependency on a collection of Bid object. Now if you want to find the highest bid for each item then Hibernate will fire 1 query to load all items and N subsequent quiries to load Bid for each item. So in order to find the highest big for each item you application end up firing N+1 quiries.
