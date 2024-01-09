# How-to-Push-projects-to-github


You can now do it right inside vscode! just follow these steps:

1- Open your new project folder with vscode

2- click on the source conrol menu on the sidebar enter image description here (or press Ctrl+Shift+G)

3- Click on publish to github enter image description here

4- From there just login and follow the instructions and you're good to go.


                      OR
                WITH TERMINAL

Here are the detailed steps needed to achieve this.

The existing commands can be simply run via the CLI terminal of VS-CODE. It is understood that Git is installed in the system, configured with desired username and email Id.

Navigate to the local project directory and create a local git repository:

git init

Once that is successful, click on the 'Source Control' icon on the left navbar in VS-Code.One should be able to see files ready to be commit-ed. Press on 'Commit' button, provide comments, stage the changes and commit the files. Alternatively you can run from CLI

git commit -am "Your comment"

Now you need to visit your GitHub account and create a new Repository. Exclude creating 'README.md', '.gitIgnore' files. Also do not add any License to the repo. Sometimes these settings cause issue while pushing in.

Copy the link to this newly created GitHub Repository.

Come back to the terminal in VS-CODE and type these commands in succession:

git remote add origin <Link to GitHub Repo> //maps the remote repo link to local git repo

git remote -v //this is to verify the link to the remote repo

git push -u origin master // pushes the commit-ed changes into the remote repo

Note: If it is the first time the local git account is trying to connect to GitHub, you may be required to enter credentials to GitHub in a separate window.

You can see the success message in the Terminal. You can also verify by refreshing the GitHub repo online.
