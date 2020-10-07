<h1 align=center><b><i>Full Stack WD</i></b></h1>

## Basic Git Commands
- At a convenient location on your computer, create a folder named git-test.
- Open this git-test folder in your favorite editor.
- Add a file named index.html to this folder, and add the following HTML code to this file:

```
<!DOCTYPE html>
<html>
    <head></head>

    <body>
        <h1>This is a Header</h1>
    </body>
</html>
```
Initializing the folder as a Git repository

- Go to the git-test folder in your cmd window/terminal and type the following at the prompt to initialize the folder as a Git repository:

```
git init
```

Checking your Git repository status
- Type the following at the prompt to check your Git repository's status:

```
git status
```

Adding files to the staging area

- To add files to the staging area of your Git repository, type:

```
git add .
```

Commiting to the Git repository

- To commit the current staging area to your Git repository, type:

```
git commit -m "My first commit"
```

Checking the log of Git commits

- To check the log of the commits to your Git repository, type

```
git log --oneline
```

- Now, modify the index.html file as follows:

```
<!DOCTYPE html>
<html>
    <head></head>

    <body>
        <h1>This is a Header</h1>
        <p>This is a paragraph</p>
    </body>
</html>
```

- Add a sub-folder named templates to your git-test folder, and then add a file named test.html to the templates folder. Then set the contents of this file to be the same as the index.html file above.
- Then check the status and add all the files to the staging area.
- Then do the second commit to your repository
- Now, modify the index.html file as follows:

```
<!DOCTYPE html>
<html>
    <head></head>

    <body>
        <h1>This is a Header</h1>
        <p>This is a paragraph</p>
        <p>This is a second paragraph</p>
    </body>
</html>
```
- Now add the modified index.html file to the staging area and then do a third commit.

Checking out a file from an earlier commit
- To check out the index.html from the second commit, find the number of the second commit using the git log, and then type the following at the prompt:

```
git checkout <second commit's number> index.html
```

Resetting the Git repository
- To discard the effect of the previous operation and restore index.html to its state at the end of the third commit, type:

```
git reset HEAD index.html
```
- Then type the following at the prompt:

```
git checkout -- index.html
```

- You can also use git reset to reset the staging area to the last commit without disturbing the working directory.

## Setting up an Online Git repository
- Sign up for an account either at Bitbucket (https://bitbucket.org) or GitHub (https://github.com).
- Then set up an online Git repository named **git-test.** Note the URL of your online Git repository. Note that private repositories on GitHub requires a paid account, and is not available for free accounts.

Set the local Git repository to set its remote origin

- At the prompt, type the following to set up your local repository to link to your online Git repository:

```
git remote add origin <repository URL>
```

Pushing your commits to the online repository

- At the prompt, type the following to push the commits to the online repository:
```
git push -u origin master
git push -f origin master  //if above not work used forced method
```
Cloning an online repository

- To clone an online repository to your computer, type the following at the prompt:

```
git clone <repository URL>
```

<h2 align=center><b><i>Node Js</i></b></h2>

### Download Nodejs [here](https://nodejs.org/en/download/) 

Initializing package.json
- At the command prompt in your **git-test** folder, type
```
npm init
```
- Follow along the prompts and answer the questions as follows: accept the default values for most of the entries, except set the entry point to index.html
  This should create a package.json file in your **git-test** folder.
- Installing an NPM Module

- Install an NPM module, lite-server, that allows you to run a Node.js based development web server and serve up your project files. To do this, type the following at the prompt:
```
npm install lite-server --save-dev
```
- You can check out more documentation on lite-server [here](https://github.com/johnpapa/lite-server).
- Next, open package.json in your editor and modify it as shown below. Note the addition of two lines, line 7 and line 9.

![](https://github.com/Psingh12354/Full-Stack-WD/blob/main/Weak%201/index.html)

```
{
  "name": "git-test",
  "version": "1.0.0",
  "description": "This is the Git and Node basic learning project",
  "main": "index.html",
  "scripts": {
    "start": "npm run lite",
    "test": "echo \"Error: no test specified\" && exit 1",
    "lite": "lite-server"
  },
  "repository": {
    "type": "git",
    "url": "git+https://jogesh_k_muppala@bitbucket.org/jogesh_k_muppala/git-test.git"
  },
  "author": "",
  "license": "ISC",
  "homepage": "https://bitbucket.org/jogesh_k_muppala/git-test#readme",
  "devDependencies": {
    "lite-server": "^2.2.2"
  }
}
```
