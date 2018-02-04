**What is constants folding?**
Constants folding is the process o recognizing and evaluating constant expression rather than computing them at runtime. 

    // code
    static final int a = 2;
    int b = 30 * a;
    
    // folding would create
    int b = 60;