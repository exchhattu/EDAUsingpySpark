


### Fixing UPF problem
While using user defined function (UDF), the following error was occurred
```
IllegalArgumentException: 'Unsupported class file major version 5'
```

It requires java8 version. To make java8 installation easier and avoid the conflict with already installed
java version.  

```
$ brew cask install homebrew/cask-versions/adoptopenjdk8
$ /usr/libexec/java_home -V
```

After above installation, following error will be displayed.
```
error : /Users/rojan/.jenv/versions/openjdk64-1.8.0.242: No such file or directory
```
This error can be easily solved using 
```
$ mkdir -p ~/.jenv/versions
```

* Install jenv 
```
$ brew install jenv
```

* Check existing JAVA version 
``` 
$ jenv versions
```

* Add jdk_path using jenv
```
$ jenv add <jdk_path>
$ jenv add /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home
```

```
$ jenv local 11.0.2
$ exec $SHELL -l
$ cat .java-version
```

Is ```JAVA_HOME``` set?
```
$ echo ${JAVA_HOME}
```

### Reference
1. Install [java8](https://medium.com/@brunofrascino/working-with-multiple-java-versions-in-macos-9a9c4f15615a)
2. [jenv](https://github.com/jenv/jenv)