# Gradle Project Setup Tutorial

You will be creating a Java application using Gradle build system that you can then open in Netbeans.

# Creating your homework directory

1. Open up a terminal on your desktop
1. `ls` to list the files in your working directory
1. cd into your repo, `cd firstname.lastname`
1. `cd cs313/sp20` 
1. cd into your programs directory, `cd programs`
1. `mkdir hw--` , where -- represents the assignment number.
1. `cd hw--`

# Get the Gradle Going

1. Inside of the hw-- directory, `gradle init` to initialize gradle
This will prompt you for what kind of project to generate. 

1. Select `application (2)`
This will prompt you for what language to use.

1. Select `Java (3)`
This will prompt you for the build script DSL.

1. Select `Groovy (1)` or hit enter.
This will prompt you for the test framework.

1. Select `JUnit4 (1)` or hit enter.
You will then be prompted for the project name. Name accordingly.

1. Project name : `projectName`
You will then be prompted for the name of your source package. Name accordingly.

1. Source package : `projectName`


# Quick Fix
A weird thing about Gradle is that there is no default input stream. That's weird. But we can amend this minor setback by opening up the build.gradle file into a text editor.

1. cd into your new project, `cd projectName`
1. `ls`. You should see several generated files, but the one we are going to look at is `build.gradle`.
1. open your build.gradle file into a text editor. I'm going to use nano because I feel like it : ) `nano build.gradle`

Within this file, you should see the plugins, repositories and dependencies sections, as well as the main class name.
You need to add the following lines to this file so your project will know that it may need to take input:

```
run{
    standardInput = System.in
}
```

That's all you need for that, so save and close your text editor.
# Build!
Yay, it exists! Now you're going to build the project. 
Make sure you are in your projectName directory. 

1. `./gradlew build` .
After your project has built, check your tasks to see what else you can do with your application.
You should see a task called `run`.

1. `./gradlew run`

If you get a Hello world, then you are successful!

You can open this project in Netbeans and begin your homework.
Good luck :)







