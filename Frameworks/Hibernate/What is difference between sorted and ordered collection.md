## What is the difference between sorted and ordered collection?

Sorted collection - collection which was sorted on Java-side.
Ordered collection - collection which was ordered on database-side.

Hibernate allows us to use ordered collection via field-annotation:

    @ManyToOne  
    @JoinColumn(name = "element_id")  
    @OrderBy("id asc ")  
    private Element element;


Or Criteria API:

    List cats = sess.createCriteria(Cat.class)
        .add( Restrictions.like("name", "F%")
        .addOrder( Order.asc("name") )
        .addOrder( Order.desc("age") )
        .setMaxResults(50)
        .list();

