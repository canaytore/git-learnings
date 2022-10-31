# Basic Git Configurations

There are three places that Git stores configuration information, and it depends on how widely we want these configurations to apply. 

- **System**: The first and broadest is the system level configuration. These are configurations that will apply to every user of this computer by default.
  - On Windows; ```C:\Program Files\Git\etc\gitconfig``` 
- **User**: Each user of course can override it with their own custom configurations, but these are the default if they don't. Now these are configurations that will apply only to a single user, which is going to be most of us most of the time, working as a single user on a machine. 
  - On Windows; ```~\.gitconfig``` or ```$HOME\.gitconfig```.
- **Project**: We can store configurations on a project basis as well. So in a single project, we can have configurations that apply only to that project.

Git provides some commands that we can use to make editing these configurations in the three different spots easy.
- **System**: ```$ git config --system```
- **User**: ```$ git config --global```
- **Project**: ```$ git config```

So what are the kinds of configurations we can set? Let's set a few. 
- ```$ git config --global user.name "Can Aytoere"```
- ```$ git config --list``` -> it will list all of my configurations
- ```$ git config user.name``` -> to look at a single configuration

Let's set the editor that we want to use. From time to time, Git is going to want to pop up and open an editor for us to be able to type some text. Mostly, to be able to type messages that we want stored in Git. 
- ```$ git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"```
- ```$ git config --global color.ui true``` -> to be able to colorize the user interface 
- ```$ cat .gitconfig``` -> to take a look at my gitconfig file

To find out more about basic configurations, see -> https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration
