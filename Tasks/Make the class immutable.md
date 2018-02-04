**Make the following class immutable**

    import java.util.Date;
    import java.util.List;
    
    public class Foo {
        private String str;
        private List<Date> dates;
    }

**Solution**

 1. Make the class `final` to forbid methods overriding and subclassing.
 2. Make instance variables `final` in order for them to be instantiated only once.
 3. We need to have a constructor with two parameters in order to pass the data to the instance. But we need to copy the data from the outside, because if we change objects from the outside we also will have changes in our immutable object.
 4. Finally, we need to copy data one more time in getter(list), because we can change the objects from the outside using list.

		public final class Foo {
		    private final String str;
		    private final List<Date> dates;

			public Foo(String str, List<Date> dates) {
			    this.str = str;
			    this.dates = Collections.unmodifiableList(dates);
			}

			public String getStr() {
			    return str;
			}

			public List<Date> getDates() {
			    return new ArrayList<>(this.dates);
			}
		}
