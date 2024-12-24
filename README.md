# Q2-Murano

<p> The objetive of this repository is to answer questions and analyse the usage of Git under various circumstances. </p>

<h2>A) Example of commands you can run with git: </h2>

<h3>1. Git Clone </h3>
<p> When a user utilizes this command, they will create a copy of a remote repository on their local machine. The command will download all the files, branches, and commit history of the repository.
<p>
When using git clone, users can pull and push their changes to the original repository. </p>
<P> Example code usage: </P>
<i> git clone "repository_url" </i>

<h3>2. Git Branch </h3>
<p> Using branches, users can create isolated workspaces for developing features, fixing bugs, and experiment withoug affecting the original code. </p>
<p> When someone creates an original git repository, they create a "main" branch. When creating additional branches, users are technically creating pointers to specific commits of the previous main branch, and therefore creating a new timeline of its own. </p>
<p> If the user wishes to do so in the future, it is possible to merge branches with the <strong> git merge </strong> command. </p>
<P> Example code usage: </P>
<i> git branch name-of-the-branch </i>

<h3> 3. Git Commit </h3>
<p> Perhaps one of the most used Git commands, <strong> Git Commit </strong> is used to save his staged changes to the local Git repository as a new version. </p>
<p> Every commit includes a unique ID (hash) and a message describing the changes. </p>
<p> As mentioned, commit only saves the changes that have been staged. To stage a change, user needs to use the <strong> git add . </strong> command. </p>
<p> Also, commiting one's change is only part of the work that needs to be done. If the user wishes to upload the changes commited to a remote repository, the <strong> git push </strong> command shall be used.</p>
<p> Example code usage> </p>
<i> git commit -m "Comment about changes" </i>

<h2>B)Solutions for having a shared library used and edited by two different projects.</h2>
<p> Now, it's time to analyze a situation where two distinct projects within the same company use and modify the same library on a daily basis. A solution is needed to ensure that the library remains synchronized with respect to each of the projects.</p> 
<p> As has been discussed, turning the library into a Git repository and creating two different branches—one for each project—will allow each project to have its own timeline and to build according to their specific needs. </p>

<h2>C) Visualizing code made in past commits, and problems generated by editing past commits directly. </h2>

![image](https://github.com/user-attachments/assets/ff334acb-bd13-4595-930b-87b6567131a8)

<p> Now, a solution is needed for when someone wants to view the code submitted on a past commit. To do so, there is a simple command: </p>
<i> git checkout (commit-hash) </i>

<p> To discover the hash of the commit in question, the following code can be ran: </p>
<p><i> git log --oneline <br> </i></p>


![image](https://github.com/user-attachments/assets/16dbafe8-9e07-4322-a156-eac2636a9495)

<p> Now, there is a situation where the user created a new commit (5) from the past commit (2), instead of returning to the present commit (4). </p>
<p>To visualize the mistake made, the user can run the following command: </p>
<p> <i> git log --graph --oneline <br> </i> </p>

<p>Now, the user can run the following code to return to the desired commit (commit 4) and import the changes made to commit 2 (that created commit 5): </p>

<i> git checkout (commit4-hash) </i>

<i> git cherry-pick (commit5-hash) </i>

<h2> D)Joining multiple commits and merging them into the main branch </h2>

![image](https://github.com/user-attachments/assets/d0170ded-5d50-4cb5-8a4f-d030e1175e06)

<p> For this part, there is a need to combine commits 5 through 8, as seen in the image above. Afterwards, the user need to merge that combination with the main branch (commit 4). </p>

<p> To do this, first the user will need to change to the latest commit (commit 8) in "branch alternativa", using the <i>git switch</i> command. </p>

<p> Next, the user needs to rebase interactively starting from commit 2 (commits 5, 6, 7, and 8). Inside the rebase editor, commits 6, 7, and 8 should be squashed (combined with the previous commit), while commit 5 should be picked (retained as it is). </p>

<p> After this is done, all the commits from the alternative branch will have been combined into commit 5. Finally, the user needs to merge the squashed commit from the alternative branch into the main branch using the git merge command. </p>
