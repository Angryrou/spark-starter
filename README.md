# spark-starter
A starting point of setting up Spark program locally on Mac Apple Silicon (M1/M2)

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
   
3. SBT build
    ```bash
    sbt package
    ```
