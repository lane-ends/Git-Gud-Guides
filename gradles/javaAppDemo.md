# Gradle Project Setup Tutorial With Gradle 6.1

You will be creating a Java application using Gradle build system that you can then open in Netbeans.
Here is a test dog. 


1. Open up a terminal on your desktop
1. `ls` to list the files in your working directory
1. `cd` into the directory you want the Gradle app to be in
1. Make a directory for your Gradle project
    - Example: `mkdir gradleProject` 
1. `cd` into your new directory

# Get the Gradle Going
1. Inside of the directory: 
    - Run `gradle init` 
        - This initializes the Gradle project.

1.  Further Prompts
    1. Select `application`
        - This will create your project.

    1. Select `Java`
        - This is the language your project will use.

    - Select `Groovy`
        - This is the Gradle DSL.

    - Select `JUnit4`
        - This sets the Java testing libraries.

    - Project name : `<project-name>`
        - The name of the project.
    -  Source package : `<source-project-name>`
        - Package names *must* be all lowercase and use dots instead of underscores, hypens, etc
         - Example:
            - `source.package`


# Using `System.in`
Gradle does not define a default input stream. That is, if you want to make use of `System.in`, you have to tell Gradle to do so within the `build.gradle` file.

From the project's root directory, open your build file, `build.gradle`, in a text editor. 

Add the following lines to this file so Gradle will know that it may need to take input:

```
run{
    standardInput = System.in
}
```
Save and close your text editor.
# Build
To build your project,
make sure you are in your project directory. 

1. Run `./gradlew build` .
    - After your project has built, check your tasks to see what else you can do with your application.
You should see a task called `run`.

1. Run `./gradlew run`
    - To tell Gradle to print less information every time it runs, use
      - `./gradlew run -q --console=plain`

If you get a Hello world, then you are successful!

Resulting Project Structure
-
![gradle picture](https://i.imgur.com/bv16NdZ.png)







