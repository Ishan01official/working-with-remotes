new file for commit
master-03 file
for practicing git
- git - - help
    
    ![image.png](attachment:ef19c803-5733-4b30-9f9e-094999e71ea2:image.png)
    
- **Why do we need version control**
    
    Version control allows you to do the same with your work—it gives you a way to save your progress. 
    
    You can do a little bit of work, save your progress, and continue working. 
    
    Which means if you make a mistake or perhaps are not happy with the current tack, you can just revert back to your previous snapshot. On the other hand, if you are happy, you just create another snapshot and keep chugging along.
    
    A version control system like Git allows you to confidently collaborate with your fellow developers over the same set of files, without stepping on each other’s toes.
    
    You can think of Git as your memory bank, safety net, and collaboration platform all built into one!
    
- Got git?
    
    ```
    Install Git
    ```
    
- What exactly is a Git repository?
    
    One reason to use a version control system is so we can save the snapshots of our work periodically. Of course, Git needs a place to store these snapshots. That place would be in the Git repository.
    
- Creating a Git repository
    
    Creating a Git repository involves running the **`git init`** command inside the top folder of your project.
    
    ![image.png](attachment:dc1d1fc7-7db1-4c6e-b1a8-a177b7b014e2:image.png)
    
- **A quick tour of the command line: knowing where you are with pwd**
    
    Start by opening a terminal window
    
    ![image.png](attachment:412c9346-e1b7-45f6-a774-a87c4599f68d:image.png)
    
    Type **`pwd`** and hit return; `pwd` stands for “**print working directory**,” and it displays the path of the directory the terminal is currently running in. 
    
    In other words, if you were to create a new file or a new directory, then they would show up in this directory.
    
    ![image.png](attachment:9fa01453-7bce-411f-a80d-5f4611ccb2b3:image.png)
    
- More on the command line: creating new directories with mkdir
    
    `mkdir` **will error out if you attempt to create a directory with a name that already exists**.
    
    *If you attempt to create a new directory with the same name as one that already exists in the current directory*, `mkdir` *will simply report* `File exists` *and not do anything. Also, don’t let the “file” in “File exists” confuse you—in this case it simply means folder*.
    
- (Even) More on the command line: listing files with Is
    
    The listing command is named `ls` (short for list).
    
    ![image.png](attachment:1e730be1-27fa-4bb1-b2be-2ecb948942ab:image.png)
    
    `ls` By default only lists regular files and folders.
    
- You want to see hidden files and folders as well. ls -A
    
    To do that, you can supply ls with a *flag*.
    Flags, unlike arguments, are prefixed with a hyphen (to differentiate them from arguments). To see “all” files and folders (including hidden ones), we can use the “A” (Yep! Uppercase “A”) flag, like so:
    
    ![image.png](attachment:f9b37ca3-2b6b-41a5-931d-c6cf676c51ae:image.png)
    
- **More on the command line (almost there): changing directories with cd**
    
    ![image.png](attachment:6c561ba7-d0fa-48c9-babd-37997dd09684:image.png)
    
    Next, moving around! We created a new directory, but how do we navigate to it? For that, we have the `cd` command, which stands for “change directory
    
    `cd ..` to go back to the parent folder.
    
- **No argument there**
    
    Command-line functions like `pwd` and `mkdir` Are the “commands” we are invoking. Some commands, like `mkdir` and `cd`, expect you to tell them what you want to create or where to go. The way we supply those is by using “arguments.”
    
    ![image.png](attachment:bd346a1f-276f-4a17-a3bc-b741a8263c5c:image.png)
    
    You might be wondering why we chose to use hyphens instead of spaces. Turns out, using spaces in arguments can get rather tricky. You see, the command line uses this to separate the command from its arguments. So, it can be super confusing to the command line if your arguments also have spaces in them.
    
    ![image.png](attachment:7b278e04-2471-4198-94d2-1f1a6e5443c6:image.png)
    
    For the command line, whitespace acts as a separator. But if we put spaces in the arguments, it’s hard for the command line to discern whether you are passing in multiple arguments or one argument with multiple words.
    
    ![image.png](attachment:4fedb6fe-5d35-4f70-bc6e-ee84eeba7539:image.png)
    
- **Who Does What?**
    
    With the command line, there are a lot of commands and flags flying around. In this game of who does what, match each command to its description.
    
    | **cd** | **Displays the path of the current directory.** |
    | --- | --- |
    | **pwd** | **Creates a new directory.** |
    | **ls** | **Navigates to the parent directory.** |
    | **mkdir** | **Changes directories.** |
    | **ls -A** | **Lists regular files in the current directory.** |
    | **cd ..** | **Lists all files in the current directory.** |
- **Creating your first repository**
    
    mkdir
    
    ![image.png](attachment:79d6904a-1696-474d-99ca-ab4369b12061:image.png)
    
    ![image.png](attachment:82b8cd96-2647-41c2-a088-31ed424f699a:image.png)
    
    ![image.png](attachment:3fefe9f8-b727-4269-9803-d972426f978b:image.png)
    
    Now that we are in a brand-new directory, let’s create our first Git repository. To do this, we simply run `git init` inside our newly created folder.
    
    ![image.png](attachment:95a8f703-b497-49f6-b1d2-03684d1a03b4:image.png)
    
- **Inside the init command**
    
    To begin with, we started with a new, empty directory.
    
    Using the terminal, we navigated to the folder location and invoked the magic words, `git init`, where `init` is short for **initialize**.
    
    Git realizes we are asking it to create a repository at this location, and it responds by creating a hidden folder called `.git` and stuffs it with some configuration files and a subfolder where it will store our snapshots when we ask it to.
    
    ![image.png](attachment:c2c2f55d-f89b-4d4e-88fd-3422e21ebe08:image.png)
    
    ![image.png](attachment:a10ec2e2-8fcc-4e49-b5e0-85e7854f2bb5:image.png)
    
    This hidden folder represents the Git repository. Its job is to store everything related to your project, including all commits, the project history, configuration files, what have you. It also stores any specific Git configuration and settings that you might have enabled for this particular project.
    
- **There are no Dumb Questions.**
    - **Q: I prefer to use my file system explorer when navigating my computer. Can I use that to see the** `.git` **folder?**
        
        **A:** Of course! By default most operating systems do not reveal hidden files and folders in the explorer. Be sure to look at your preferences and ensure that you can see hidden files and folders.
        
    - **Q: What happens if someone accidentally deletes this directory?**
        
        **A:** First of all, let’s not do that. Second, this directory is the “vault” in which Git stores all its information—including your entire project history and a bunch of other files that Git needs for housekeeping, and some configuration files that we can use to customize our experience with Git. This means that if you delete this folder, you will lose all project history. However, all the other files in your project folder will remain unaffected.
        
    - **Q: What happens if I accidentally run** `git init` **more than once in the same folder?**
        
        ***A:** Good question. This is completely safe. Git will simply tell you that it is reinitializing the Git repository, but you will not lose any data nor will you hurt anything. In fact, you should try it in `ch01_01`. We are early in our journey, and the best way to learn is to experiment. Whatcha got to lose?*
        
    - **Q: Other version control systems that I have used have a server component. Don’t we need that here?**
        
        **A:** Getting started with Git is *really* easy. `git init` creates a Git repository, and you can get to work. Eventually, you will need a mechanism to share your work with your teammates, and we promise we will get to that soon enough. But for now, you are all set.
        
- **Introduce yourself to Git**
    
    There is one more step before we get to work with Git and Git repositories. Git expects you to give it a few details about yourself. This way, when you do create a “snapshot,” Git knows who created it.
    
    We will start with our trusty old friend, the terminal, and follow along. **Be sure to use your name and email instead of ours!** 
    
    ![image.png](attachment:f924e4b9-ca28-4907-aed3-a24d3c578fef:image.png)
    
    ![image.png](attachment:20b76699-6fe5-4237-a836-e2d76df3286d:image.png)
    
- **How you will use Git**
    
    Let’s get a sense of what a typical interaction with Git looks like. Remember how we spoke about video games allowing you to save your progress? Well, asking Git to “save your progress” involves “committing” your work to Git. Essentially, this means that Git stores a revision of your work.
    
    ![image.png](attachment:200fab90-5362-49f2-91f8-d64528a686b2:image.png)
    
- **Putting Git to work**
    
    We are sure you raring to get started (we know we are!). So far, we have initialized a Git repository, told Git our name and email, and kinda sorta have a sense of how we usually work with Git. So, how about we actually put Git to work. We will start small and just put Git through its paces—we will see how to “take a snapshot” in Git by creating a “commit.”
    
    For the sake of this exercise, let’s pretend to start working on a new project. We usually start with a checklist so we can keep track of everything we have to do. As we progress with the project, we keep checking things off (gotta keep that dopamine flowing!), and as we learn more about the project, we keep adding to it. Naturally, this file is version-controlled with the rest of the files in the project, for which we will use Git.
    
    Let’s break down what we are going to do, step-by-step.
    
    **Step One:**
    
    Create a new project folder.
    
    **Note
    These two steps should be pretty familiar to you.**
    
    **Step Two:**
    
    Initialize a Git repository within that folder.
    
    **Note
    These two steps should be pretty familiar to you.**
    
    **Step Three:**
    
    Create our checklist with a few items to get us started.
    
    **Step Four:**
    
    Store a snapshot of our checklist in Git by committing the file.
    
    **Note
    Now that’s what we have been waiting for!**
    
- **Meanwhile, back at the HawtDog Dating Service...**
    
    ![image.png](attachment:d4640576-1c26-41fa-99e9-e90705dbfe3b:image.png)
    
- **Working with the HawtDawg Git repository**
    
    Next, create a new document in your favorite text editor, and type in the following lines of text. If you followed the instructions in the introduction to install Visual Studio Code, then just like the terminal, you will find **`Visual Studio Code.app`** under the **`Applications`** folder. In Windows, just click on the Start menu and you should see Visual Studio Code listed under all the applications installed on your machine.
    **Note**
    
    To create a new file, simply click on the File menu item at the top and pick “New File.”
    
    ![image.png](attachment:055ea794-1bba-4045-b839-8a47faf7dfed:image.png)
    
    Save the file as **`Checklist.md`** in the **`HawtDawg`** directory.
    
    Now we are ready to commit our work. This involves two Git commands, namely **`git add`** and **`git commit`**.
    
    ![image.png](attachment:566d28ee-4544-403e-9a14-1ff9afa4cd38:image.png)
    
    Notice that the `git add` The command takes as its argument the name of the file you wish to add to Git.
    And the `git commit` The command has a flag, `-m`, followed by the commit message. 
    The -m stands for “message” and is a mechanism for you to provide a meaningful reminder as to why you made this change.
    
    **Note**
    
    ```
    You can also use the longhand version of -m, like so—git commit --message followed by the message. We like the shorter version though.
    ```
    
- **There are no Dumb Questions**
    - **Q: Do I need to use Markdown files? I thought Git was a general-purpose version control tool.**
        
        **A:** Oh, no! We are only using Markdown files to make things easy. Teams use Git to version all kinds of different files, including source code, journals, to-do lists, blog posts, what have you. You see, Git is exceptionally good at working with plain-text files—like Markdown, HTML, source code for programming languages like Python—as opposed to rich text (like you would get out of Microsoft Word or Apple Pages). Just know Git is extremely flexible and can accommodate lots of different kinds of files.
        
- **Did you get some other output than the one we showed you in the previous exercise?**
    
    ***The command line can be rather unforgiving when it comes to typos, whitespace, and casing. If you did not get the same output as ours, then here are a few things to try:***
    
    - ***If you see an error like* `fatal: not a git repository`, *be sure that you are in the* `HawtDawg` *directory*.**
    - ***If you got an error like* `command not found,` *then be sure to check to make sure you got the case and the spelling right. Usually the command line tells you which command it did not recognize*.**
    - ***If you see an error along the lines of* `fatal: pathspec checklist.md did not match any files` *when you tried a* `git add`, *know that the filename you supply needs to match the filename exactly, which in our case would be Checklist.md (uppercase “c”)*.**
    - ***If you get* `error: pathspec ‘-’ did not match any file(s) known to git` *when trying to* `git commit`, *make sure that there is no space between the*  *and* `m`.**
    - ***If the command line reports an error like* `error: pathspec ‘first’ did not match any file(s) known to git`, *make sure to wrap the commit message “My first commit” in double quotes*.**
    - ***If you get an error like* `nothing added to commit but untracked files present`, *then try running* `git add Checklist.md` *again, this time making sure you get the filename correct, including the casing*.**
- **What exactly does it mean to commit?**
    
    We learned that committing to Git is a two-step process. You first `add` the files and then `commit`.
    
    The first thing to know is that only the files that you add are committed. Let’s say you had two files, `Checklist.md` and `README.md`, but you only added `Checklist.md`. When you create a commit, Git will **only** store the changes made to `Checklist.md`.
    
    Now, when we commit, Git uses a specialized algorithm to safely tuck away everything that we added to its memory. When we say we “committed” our changes to Git, what that translates into is that Git creates a **commit object** that it stores inside the `.git` folder. This commit object is “stamped” by a unique identifier. You might recall that we got `513141d` when we made our commit in our last exercise (you certainly saw something different)—this is actually a much longer string containing numbers and letters that looks something like this:
    
    ![image.png](attachment:4dbd0e02-2907-4776-9fe1-de83fc9adff8:image.png)
    
    **This identifier is computed using a bunch of metadata**, including your full name, the time as it was when you made the commit, the commit message you provided, and information derived from the changes you committed.
    
- **Look before you leap**
    
    You just made your first commit. Making a commit involves two separate commands—**`git add`** followed by **`git commit`**. You are probably wondering why it takes two commands to make a commit in Git—why does Git make us jump through all these hoops so we can store a revision of our work in Git?
    
    The answer lies in the design of the Git repository. Remember that the Git repository is housed in the `.git` A folder that gets created when you run `git init`.
    
    The Git repository itself is divided into two parts—the first part is called the “index,” and the second part is what we will refer to as the “object database.”
    
    When we run `git add <filename>`, Git makes a copy of the file and puts it in the index. We can think of the index as the “staging area,” wherein we can put things till we are sure we want to commit to them.
    
    Now, when we run the `git commit` command, it takes the **contents of the staging area** and stores those in the object database, also known as Git’s memory bank. To put it another way, the index is a place to temporarily house changes. Typically, you make some changes, add them to the index, and then decide if you are ready to commit—if yes, then you make a commit. Otherwise, you can continue making changes, add more changes to the staging area, and then, when you feel you are in a good place, commit.
    
    ![image.png](attachment:85164931-dc5a-4d97-b1ec-36b40a178c60:image.png)
    
- **The three stages of Git**
    1. Let’s start at the top. We have a working directory with just one file.
    
    ![image.png](attachment:e10c7b2a-a2ba-481e-9280-132bd2ec79a4:image.png)
    
    1. When we `git add Checklist.md`, Git stores a **copy** of that file in the index.
    
    ![image.png](attachment:df00091c-ea7f-454b-80cb-bd71960f7b72:image.png)
    
    1. Finally, when we commit, Git creates a commit object that records the state of the index in its memory.
    
    ![image.png](attachment:f6082db5-6446-40e8-94be-94d06930b358:image.png)
    
- **Git in the command line**
    
    Git uses the `git` command, usually followed by a “subcommand,” like `add` or `commit`, and finally followed by arguments to the *subcommand*.
    
    ![image.png](attachment:834488eb-65d5-4869-9d67-a09b019d079f:image.png)
    
    Finally, `git commit` takes both a flag, `-m`, and a message. `-m` is a flag, and here, we should **not** put a space between the hyphen and `m`.
    
- **The multiple states of files in a Git repository**
    
    Here is what a typical interaction with Git looks like: you make some edits to one or more files, then add them to the index, and when you are ready, you commit them. Now, as you are going through this workflow, Git is attempting to track the state of your files so it knows which files are part of your working directory, which files have been added to the index, and which files have already been committed to its object store.
    
    ![image.png](attachment:5eb82b46-887c-478d-8fef-af8173643c13:image.png)
    
    **But there’s more. A file may move through all the various stages, but it could be in more than one state simultaneously!**
    
- **The index is a “scratch pad”**
    
    Let’s revisit the role of the index. We know that as we edit files in our working directory, we can `add` them to the index, which marks the file as “staged.”
    
    ![image.png](attachment:123cf3e6-a3e2-42a6-af83-0a26ef4e6dd3:image.png)
    
    Of course, we can continue editing the file even after adding it to the index. Now, we have two versions of the file—one in the working directory and one in the index.
    
    ![image.png](attachment:b08468e4-6c49-4337-ad8d-e7b35a4c8558:image.png)
    
    Now if you add the file again, Git ***overwrites*** the index with the latest changes reflected in that file. In other words, the index is a temporary scratch pad—one you can use to stuff edits into till you are sure you want to commit.
    
- **Computer, status report!**
    
    As you continue to work with Git, it’s often useful to check the status of the files in your working directory. One of the most useful commands in your Git arsenal is the **`git status`** command. This command is particularly useful as your project grows in size, with multiple files.
    **Note**
    
    Remember that the working directory is the directory containing the hidden .git folder.
    
    So let’s explore how to use the status command: you’ll create Yet Another Git Repository™, except this time you will create multiple files in your repository. This will give you a chance to see what `git status` reports and get an intuitive sense of how Git works.
    
    As you have done before, you will create a brand-new folder inside the umbrella `headfirst-git-samples` folder called **`ch01_03`**, and initialize a Git repository inside that folder.
    
- **You’ve made history!**
    
    We know that Git commits record the changes you made and added to the index, along with some metadata—like information about the author (you) as well as the commit message. There is one final detail about commits that you ought to know about. For every commit that you make (other than the very first one in a repository), the commit also records the commit ID of the commit that came just before it.
    
    ![image.png](attachment:401d0aaa-d279-411d-a766-508763f1cd1f:image.png)
    
    That is to say, the commits form a chain, much like the branch of a tree, or a string of Christmas lights. This means, given a commit ID, Git can trace its lineage by simply following the “parent” pointer. This is referred to as the **commit history** and is an integral piece to how Git works.
    
- **Bullet Points**
    - A version control system like Git allows you to store snapshots of your work.
    - Git is much more than a tool that allows you to record snapshots. Git allows us to confidently collaborate with other team members.
    - Using Git effectively requires you to be comfortable with the command line.
    - The command line offers a slew of other capabilities, including creating and navigating directories and listing files.
    - Git is available as an executable, which you install, and it makes Git available to use in the command line with the name `git`.
    - Once you install Git, you need to tell Git your full name and your email address. Git will use this whenever you use Git to take a snapshot of your work.
    - If you want Git to manage the files for any project, we have to initialize a Git repository at the root level of the project.
    - To initialize Git you use the init command, like so: `git init`
    - The result of initializing a new Git repository is that Git will create a hidden folder called `.git` in the directory where you ran the `git init` command. This hidden folder is used by Git to store your snapshots, as well as some configuration for Git itself.
    - Any directory that is managed by Git is referred to as the working directory.
    - Git, by design, has an index, which acts as a “staging area.” To add files to the index, you use the `git add <filename>` command.
    - Committing in Git translates to taking a snapshop of the changes that were stored in the index. The command to create a commit is `git commit`, which requires that you supply it with a commit message to describe the changes you are commiting, using the `m` (or `-message`) flag:
        
        **`git commit -m “some message”`**
        
    - Every file in the working directory is assigned one or more states.
    - A brand new file added to the working directory is marked as “untracked,” which suggests that Git does not know about this file.
    - Adding a *new* file to Git’s index does two things—it marks the file as being “tracked” and creates a copy of that file into the index.
    - When you make a commit, Git creates a copy of the files in the index and stores them in the object database. It also creates a commit object that records metadata about the commit, including a pointer to the files that were just stored, the author name and email, and the time the commit was made, as well as the commit message.
    - Every commit in Git is identified by a unique identifier, refererred to as the commit ID.
    - At any time you can ask Git for the status of the files in the working directory and the Git repository, using the `git status` command.
    - Every commit **except** the initial commit in Git stores the commit ID of the commit that appeared just before it, thus creating a string of commits, like leaves on a branch.
    - This string of commits is referred to as the commit history.
- **Sharpen your pencil**
    
    In the terminal window you have open,
    
    Go ahead and use `mkdir` to create a new directory called `my-first-commandline-directory`
    
    ![image.png](attachment:5d9f3897-7b0d-4fae-adee-10999342ffa4:image.png)
    
    ![image.png](attachment:83b00236-eadb-494b-82ce-651d191e1dc1:image.png)
    
    Next, run the same command again, in the same directory. Write down the error you see here:
    
    ![image.png](attachment:0830aadc-959e-4d8d-9818-4339674684f2:image.png)
    
    Use the terminal to list all the files in the current directory. See if you can find your recently created `my-first-commandline-directory`.
    
    ![image.png](attachment:b24c55f6-a19f-4660-8b80-edcde37b239f:image.png)
    
    Then use the `-A` flag and see if there are any hidden folders in the current directory.
    
    ![image.png](attachment:57d53ed4-5d2f-463a-b37e-43099021ec16:image.png)
    
    **You create a new file in the repository called** `Hello.txt`.
    
    ![image.png](attachment:3e9ec64c-34bc-4956-931f-ff3685f8e624:image.png)