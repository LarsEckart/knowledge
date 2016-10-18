# Java

## Javadoc

How to link to methods or classes

```
{@link package.class#member label}
```

## UNIX TOOLS TO TROUBLESHOOT JAVA

### jps – java process information

```
jps
```
It lists all java-processes.

[Documentation](http://docs.oracle.com/javase/7/docs/technotes/tools/share/jps.html)

### lsof – List of open files

```
lsof -p <pid>
```

Given the process id, it shows every file that is opened by that process.

### jstack

```
jstack <pid>
```
It dumps out all threads and what they are doing

## Testing

### How to test that an exception is thrown

[expected exception in test](https://monkeyisland.pl/2010/07/26/expected-exception-in-tests/)
