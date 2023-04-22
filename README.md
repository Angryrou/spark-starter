# spark-starter
A starting point of setting up Spark program locally on Mac Apple Silicon (M1/M2). 
We target on using the Spark version 3.2.1, JDK8, Scala 2.12, SBT 1.5.7.

1. JDK 8 (Zulu Community 8)
    ```bash
    brew tap homebrew/cask-versions
    brew install --cask zulu8
   
    # add under ~/.zshrc or ~/.bashrc
    export JAVA_HOME=`/usr/libexec/java_home -v 1.8`
    # Please note that Zulu Community 8 will only be supported until March 2026.
    ```

2. Scala 2.12
    ```bash
    brew install scala@2.12.17
    ```
   
3. SBT build (1.5.7)
    ```bash
   sbt package
   [info] welcome to sbt 1.5.7 (Azul Systems, Inc. Java 1.8.0_362)
   [info] loading global plugins from /Users/chenghao/.sbt/1.0/plugins
   [info] loading project definition from /Users/chenghao/ResearchHub/repos/blogs/test/spark-starter/project
   [info] loading settings for project spark-starter from build.sbt ...
   [info] set current project to Simple Project (in build file:/Users/chenghao/ResearchHub/repos/blogs/test/spark-starter/)
   [info] compiling 1 Scala source to /Users/chenghao/ResearchHub/repos/blogs/test/spark-starter/target/scala-2.12/classes ...
   [success] Total time: 3 s, completed Apr 22, 2023 2:53:06 PM
    ```

4. Run/Debug in Intellij
   - Set JDK 8 and scala 2.12.17 in IJ project environment
   - Hard-code the `spark.master` as `local[4]` in the program when starting a Spark session
   - Run/Debug directly in Intellij
