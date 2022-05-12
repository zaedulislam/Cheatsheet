
#### To list all versions of installed JDK
```
admins-MacBook-Pro-4:/ zaedulislam$ /usr/libexec/java_home -V
Matching Java Virtual Machines (4):
    17.0.3 (x86_64) "Eclipse Adoptium" - "OpenJDK 17.0.3" /Library/Java/JavaVirtualMachines/temurin-17.jdk/Contents/Home
    1.8.333.02 (x86_64) "Oracle Corporation" - "Java" /Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home
    1.8.0_333 (x86_64) "Oracle Corporation" - "Java SE 8" /Library/Java/JavaVirtualMachines/jdk1.8.0_333.jdk/Contents/Home
    1.7.0_80 (x86_64) "Oracle Corporation" - "Java SE 7" /Library/Java/JavaVirtualMachines/jdk1.7.0_80.jdk/Contents/Home
/Library/Java/JavaVirtualMachines/temurin-17.jdk/Contents/Home
```

#### To verify manually, by going to the specific location and then check. To do this run below command in the mac terminal
```
cd /Library/Java/JavaVirtualMachines/
```
Then run `ls` command in the terminal again. Now WE can see the jdk version & package if exists in the computer.
