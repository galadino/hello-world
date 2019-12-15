# hello-world
just a test

## Now working on branch joking

# Now let's use the command line (this gui sucks)
As a first example we start from an existing project. In github terminology we clone a repository.
It is as simple as that
```
$ git clone git@github.com:galadino/hello-world.git
```
If you add your ssh key from the web interface, this will go smooth with no password request.
This is done from the 'SSH and GPG keys' entry from the 'setting' menu from your profile icon.

Now we go this new folder and make some edits to the README.md file and then we commit all these changes.
```
$ git add --all
$ git commit -m "began cli work"
[master 12b9b67] began cli work
 1 file changed, 11 insertions(+)
```
Our version is still on our PC, to make the version available on github we need to push it on the server.
```
$ git push origin master
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 607 bytes | 607.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:galadino/hello-world.git
   888e971..12b9b67  master -> master
```
Now try to refresh the web page. You can see all edits done. Let's say that we are satisfied by this version and we want to begin to work on a new feature.
Let's start a new branch
```
$ git branch my_feature
```
Let's switch to the new branch
```
$ git checkout my_feature
Switched to branch 'my_feature'
```
We make some work and when we are satisfied we commit it
```
$ git add --all
$ git commit -m "working on my_feature"
[my_feature 851ff4c] working on my_feature
 1 file changed, 14 insertions(+), 1 deletion(-)
```
When we are satisfied by my_feature we can merge is to the master branch. We first switch back to master branch:
```
git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
```
And then push my_feature to github
```
git push origin my_feature
```
