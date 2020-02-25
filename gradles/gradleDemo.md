# Gradle Project Setup Tutorial With Gradle 6.1

You will be creating a Java application using Gradle build system that you can then open in Netbeans.
Here is a test dog. 
![dog image](https://d17fnq9dkz9hgj.cloudfront.net/breed-uploads/2018/09/dog-landing-hero-lg.jpg?bust=1536935129&width=1080)

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







