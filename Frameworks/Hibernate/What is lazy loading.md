## What is lazy loading?
Say you have a parent and that parent has a collection of children. Hibernate now can "lazy-load" the children, which means that it does not actually load all the children when loading the parent. Instead, it loads them when requested to do so. You can either request this explicitly or, and this is far more common, hibernate will load them automatically when you try to access a child.

Lazy-loading can help improve the performance significantly since often you won't need the children and so they will not be loaded.

Also beware of the n+1 problem. Hibernate will not actually load all the children when you access the collection. Instead, it will load each child individually. When iterating over the collection, this causes a query for every child. In order to avoid this, you can trick hibernate into loading all children simultaneously, e.g. by calling `parent.getChildren().size()`.
