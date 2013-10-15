sandbox-sample-maven

test 1 ubuntu
111

This is a sample project that demostrates usage of maven with GWT.


This project was imported by Eclipse because Cloud IDE does not provide a ready sample using 
the latest GWT libraries.


Step 1. Using Maven in your system, create an archetype - this is a gwt project created by maven
ready to be imported into Eclipse.

    To do this, following the instructions from: http://mojo.codehaus.org/gwt-maven-plugin/user-guide/archetype.html
    execute: 
        mvn archetype:generate \
       -DarchetypeGroupId=org.codehaus.mojo \
       -DarchetypeArtifactId=gwt-maven-plugin \
       -DarchetypeVersion=2.5.1

    The output of the project that we created (and use here is found in file maven_sample_output.txt)


    This will create the project and all you have to do is import it into Eclipse as a project with existing 
    resources.

    Note: You may get an error regarding the use of Message.class. I deleted all statements that used the class
    and entered text manually which resolved this issue. 


Step 2. Create a google app engine sample project. 

    Cloud IDE will create a sample project, but it is not using the latest GWT libraries and folder structure.
    Since we now have the working Eclipse GWT-Maven project, we zip up the java, resources, and webapp folders
    and pom.xml and upload them into the project (deleting the previous folders created by Cloud IDE).

    In this way the Cloud IDE project will now contain the project we previously created in Eclipse and 
    we can enjoy coding away... :).


Step 3. Start expanding the project and adding any new libraries in the pom.xml. Check out 
http://maven.apache.org/guides/getting-started/index.html for more info on Maven.

In brief, Maven has this pom.xml that defines all libraries that the project needs and helps us
build the project in a more organized way (versioning, modules, artifacts etc).



