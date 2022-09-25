
# Install Spark (and PySpark) on a Mac

https://spark.apache.org/docs/latest/
- Spark runs on Java 8/11, Scala 2.12/2.13, Python 3.6+ and R 3.5+







https://notadatascientist.com/install-spark-on-macos/





chmod +x /usr/local/Cellar/apache-spark/3.2.1/libexec/bin/*


chmod +x /opt/homebrew/Cellar/apache-spark/3.2.1/libexec/bin/*


chmod +x /opt/homebrew/Cellar/apache-spark/3.2.1/libexec/bin/*

/opt/homebrew/Cellar/openjdk/18

"terminal.integrated.env.osx": {
    "SPARK_HOME": "/opt/homebrew/Cellar/apache-spark/3.2.1/libexec"
  }


  ### Installing Java 8/11

  For the system Java wrappers to find this JDK, symlink it with
  sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk

openjdk@11 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have openjdk@11 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/openjdk@11/bin:$PATH"' >> ~/.zshrc

For compilers to find openjdk@11 you may need to set:
  export CPPFLAGS="-I/opt/homebrew/opt/openjdk@11/include"

```
brew install openjdk@11
brew install scala@2.13
brew install apache-spark

```
# symlink required to find Java Runtime
sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk

/opt/homebrew/Cellar/openjdk@11/11.0.14.1


### Understanding Symlinks
https://www.imore.com/how-use-symbolic-links-macos-load-balance-your-data

https://stackoverflow.com/questions/58314491/what-is-the-purpose-of-creating-a-symbolic-link-between-files