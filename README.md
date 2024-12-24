# Q2-Murano

<p> The objetive of this repository is to answer questions and analyse the usage of Git under various circumstances. </p>

<h2> Examples of commands you can run with git: </h2>
<h3> Git Clone </h3>
<p> When an user utilizes this command, he will create a copy of a remote repository on his local machine. The command will download all the files, 
branches and commite history of the repository. </p>
<p> When using git clone the users can pull and commit their codes to the original repositories. </p>
<P> Example code usage: </P>
_ git clone "repository_url" _

<h3> Git Branch </h3>
<p> Using branches, users can create isolated workspaces for developing features, fixing bugs, and experiment withoug affecting the original code. </p>
<p> When someone creates an original git repository, they create a "main" branch. When creating additional branches, users are technically creating pointers to specific commits of the previous main branch, and therefore creating a new timeline of its own. </p>
<p> If the user wishes to do so in the future, it is possible to merge branches with the **git merge** command. </p>
<P> Example code usage> </P>
_ git branch name-of-the-branch_
