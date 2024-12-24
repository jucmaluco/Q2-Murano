# Q2-Murano

<p> The objetive of this repository is to answer questions and analyse the usage of Git under various circumstances. </p>

<h2> Example of commands you can run with git: </h2>

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
