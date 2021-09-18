## Lox Online
Lox Online is an online compiler for a custom language interpreter I wrote over the summer ([github link](https://github.com/HUNTINGHOUND/cpplox)). The online interpreter should support users writing code inside a web-based editor and run it whenever they like. It should also support saving, upload, deleting, and downloading files (like google doc) and a stand-alone Lox repl console (similar to the python console).

Lox is a very simple dynamically typed language intended to introduce people to the world of computer programming. Its easy-to-use syntax and functionality allow it to be a perfect bridge from knowing nothing about programming to understanding basic concepts. Lox Online allows users to skip the annoying steps of building, configuring, and setting up runtime environments and go straight to learning. 

### Target Audience
People who want to learn computer programming or people who know a bit about programming and want to write a quick script for various tasks.

### User experience
The user should be greeted with a straightforward text editor and output component. The user should be able to run the code without logging into his account. When the user is logged in, there should be an option for the user to go to a separate interface where they can see all their saved files. They can save, edit and delete those files however they like. To run their Lox program, the user should simply click a run button and the output will display on the output window. There should also be a repl console that can be activated with a button that allows users to write simple code that requires minimal syntax. 

### Scope
Lucky for you, I have already written the Lox Interpreter over last summer. It's completely usable and we just have to find a way to get the user's input into the interpreter and display the result. Of course, handling accounts and file storage is a whole different thing but I believe it can be easily achieved. Since this has been a project I wanted to do regardless, I have already done most of the researches needed for this project. I just wrote this simple Flask API structure today that will define our backend API ([github link](https://github.com/HUNTINGHOUND/loxonline-api)). Furthermore, if this turns out to be too easy, there are plenty of things we can add. For example, collaboration in a single file, syntax highlighting, static analysis of code, workspace creations, support of other languages .etc

### Techstack
I thought I would introduce the tech stack since this project will require many different components and I don't want you to join the team and then realize you don't know how to use anything.

AWS (ec2 and s3): I know the professor mentioned Digital Ocean. After some research, I found a couple of problems with Digital Ocean. First, it does not support dynamic applications for free. This means someone must pay to host the python backend API. I rather move to a slightly more complicated platform than deal with money issues. AWS free tier allows acceptable free usage of EC2 which should be enough for this application. Second, Digital Ocean's file storage capacity is not very well documented. Compared to S3 (Amazon's storage solution), which is much better documented and with more existing libraries, Digital Ocean seems like a subpar choice. AWS might be jarring but it's not that difficult to learn as long as you don't mess with things you don't need.

Python Flask: I don't know Django, probably should learn it. With that being said, Django is heavy and overkill for our simple python API. I've already done most Flask-orientated things in the structure, but some basic understanding of how Flask works and how to use it can go a long way.
