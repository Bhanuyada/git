1.first of all setup a remote Repository in local system..
    - initialize a local Git Repository using (( git init ))
    - add a remote repository: (( git remote add origin URL ))

2. Add a file, commit and push to master Branch.....
    - creating a new file (( echo " bhanu pratap " > bhanu.txt ))
    - Add the file to the staging area: (( git add bhanu.txt ))
    - commit the changes: (( git commit -m "Add bhanu.txt"
    - push the change to the master branch: (( git push -u origin master ))

3. Create a new Branch, Commit and push Changes.....
    - create a new branch: (( git checkout -b new-feature ))
    - add a new file: (( echo "new feature" > feature.txt ))
    - add the file to the staging area: (( git add feature.txt ))
    - commit the changes: (( git commit -m "Add feature.txt" ))
    - push the changes to the new branch: (( git push -u origin new_feature ))

4. merge new branch with master branch using pull request:
    - Create a pull request on your Git hosting service.....
         Navigate to the repository on the hosting service.
         Click on "New Pull Request".
         Select new-feature as the branch to merge into master.
         Create the pull request and merge it.

5.  undo the Last Commit or Remove the Last Created File from Remote Repo..
    - undo the  last commint (( git reset --soft HEAD~1 ))
    - Remove the last created file.
           - git rm feature.txt
           - git commit -m "Remove feature.txt"
           - git push origin new-feature

6. Resolve a merge conflict..
   a. - create a merge conflict..
        - modify "bhanu.txt" on master and commit:
           - echo "Change in master" > bhanu.txt
           - git add bhanu.txt
           - git commit -m "Change in master"
           - git push origin master
        - modify "bhanu.txt " on new feature and commit..
           - git checkout new-feature
           - echo "Change in new-feature" > bhanu.txt
           - git add bhanu.txt
           - git commit -m "Change in new-feature"
           - git push origin new-feature

     b. - Attempt to merge new feature into master...
         - git checkout master
         - git pull origin master
         - git merge new-feature

     c. Resolve the merge conflict:
          - open the conflicted file bhanu.txt in an editor.
          - edit the file to resolve the conflicts
          - add the resolved file..(( git add bhanu.txt ))
          - commit the merge:  (( git commit -m "Resolve merge conflict" ))
     d. Push the changes:
          - git push origin master


Some other git hub command like:-


                 
