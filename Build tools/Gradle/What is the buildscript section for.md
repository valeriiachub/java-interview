**What is the buildscript section for?**

The `buildscript` block determines which plugins, task classes, and other classes are available for use **in the rest of the build script**. Without a `buildscript` block, you can use everything that ships with Gradle out-of-the-box. If you additionally want to use third-party plugins, task classes, or other classes (in the build script!), you have to specify the corresponding dependencies in the `buildscript` block.

Technically speaking, Gradle needs this information in order **to compile and evaluate the rest of the build script**.