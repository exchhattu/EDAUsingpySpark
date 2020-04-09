
While using user defined function (UDF), the following error was occurred
```
IllegalArgumentException: 'Unsupported class file major version 5'
```

Solution, it required old java

I am not intersted to mess up my 

brew install jenv

brew cask install homebrew/cask-versions/adoptopenjdk8
/usr/libexec/java_home -V

n: /Users/rojan/.jenv/versions/openjdk64-1.8.0.242: No such file or directory
mkdir -p ~/.jenv/versions

jenv add /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home
penjdk64-1.8.0.242 added
1.8.0.242 added
1.8 added

$ jenv versions

Reference

1. java8 (https://medium.com/@brunofrascino/working-with-multiple-java-versions-in-macos-9a9c4f15615a)