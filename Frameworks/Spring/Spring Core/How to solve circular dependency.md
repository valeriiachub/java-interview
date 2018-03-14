## How to solve circular dependency?

First of all, we can have circular dependency only in a case of constructor injection. As many knows, the first step of any bean lifecycle if to instantiate java object via reflection. If we don't have dependency at the time Spring will try to instantiate that dependency but, obviously, will fail.

Workarounds:
1. Redesign your system.
2. @PostConstruct + Setter.
3. Setter/field injection.
4. @Lazy for one of the beans(proxy will be created).
