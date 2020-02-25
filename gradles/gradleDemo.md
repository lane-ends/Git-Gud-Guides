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

    - Project name : `<project-name>`
        - The name of the project.
    -  Source package : `<source-project-name>`
        - Package names *must* be all lowercase and use dots instead of underscores, hypens, etc
         - Example:
            - `source.package`


# Using `System.in`
Gradle does not define a default input stream. That is, if you want to make use of `System.in`, you have to tell Gradle to do so within the `build.gradle` file.

From the project's root directory, open your build file, `build.gradle`, in a text editor. 

Within this file, you will see the plugins, repositories and dependencies sections, as well as the main class name.
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







