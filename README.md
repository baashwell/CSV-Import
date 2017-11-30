# CSV-Import
Java Refresh CSV Importing


Training project for Maven and Visual Studio Code.

1) Installation and Git Link

    Installing VSC, JDK, JRE, GIT and Maven is all simple enough ensuring that you add the correct PATH values. Git integration with VSC can be done via using the standalone GIT Bash shell to pull down projects, edit the repository and use the shell to push again.

    I have choose to pull using VSC via opening the command window (CTRL+SHIFT+P) and entering Git Clone, followed by the URL and then the location to store the repository. All of this is assuming you have installed the Visual Studio Team Services add on.

    Commit and Pushing can then be done via the Version control system within VSC, although not on the WIFI in Fenchurch Street office. Firstly, save the file you are working on and stage it (right click stage), once staged on the version control tab press the tick to commit changes and then at the bottom right hand corner you can press arrow button to push changes.

    https://code.visualstudio.com/docs/editor/versioncontrol

2) Maven Generation

    Once Maven is installed you can use it to set up the project for you via the CMD. Use the following command to create a project (called my-app in this case). 

    mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

    https://gorkem1.gitbooks.io/visual-studio-code-for-java/chapter-1/Maven-Create.html

    There was an issue with JUNIT on creation, giving an erro "Failed to read artifact descriptor for junit:junit:jar:3.8.1" and "Missing artifact junit:junit:jar:3.81"


3) CSV Parsing

    Read around to view current simple solutions that are not just "split on ,"; found https://agiletribe.wordpress.com/2012/11/23/the-only-class-you-need-for-csv-files/ that gives a fairly simple implementation that gave me ideas on implementing my own as a test to ensure all is working on this set up and to get up to speed with using Maven and VSC.

    Wrote a list of basic features that will most likely be broke down even further as each is picked up.

    3.1) Open a CSV file

        First feature picked up is to simply open a CSV, splitting down into the following tests:
        - Open a CSV
        - Do not attempt if not a CSV
        - Do not fail if cannot find/open

        Created a class - StatementReader and mirror test class.
