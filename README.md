# git-practice
- few developers are joining to our project we dont want changes into master directly master always points to production
- master ---> production (not allowed directly to push into proudction)
- take another copy --> edit that --> check once again and make its main copy (this is the general practice in every where)
- create another copy --> do the chages --> do some checks --> if everything fine then merge in to master
- if we wants to merger we need to rise the pull request (pr) so the team lead will review what are the changes done at-least we nedd to get approve from two members in the project 
- even team leader doesnt have access to push directly to the master we need pr before merging
- add the team memebers and give acces if he want to approve merge give him write access
- no one is allowed to push changes in master so create feature-1
- git branch feature-1 (to create branch)
- git checkout feature-1 (to checkout new branch)
- push to the feature branch
- git log  
- commit id contains 40 characters sha code

![alt text](deshi/Downloads/Screenshot 2024-12-18 124933.png)

- if the team member wants to rise the pull request
- open the master branch it will show the pop up like compare and merge the request from feature to master and write some comment like "hi i developed some new feature its good to merge with master" after that we need to get aprove from the team who has acces to approve we have team leader so he will click on the pull request and he will undertand the commits and file changes in that and the team leader will review the changes and he may give 'comment','approve','request changes'
so if all good he may approve if not request-to change some thing and submit review.
- After getting approve from the team leader he can see that the 'merge pull request','squash and merge','rebase and merge' 
```
as a team memeber create feature branch and do changes 
raise pr(pull request)
you can ask team members to review, once you once you get approval you can merge into master
always pull before you push
```

#### merge pull request
- let us understand the merge pull request
- for merge having two parents like last commits and merge commit ids
- last commit id is the parent for feature and merge is also given one commit id
- when we do merge we will get new commit id depeicting the merge 
- history is preserved 
- it will safe guard the history 
```
again one new feature branch is created so again rise the pr and review it and create pull request and if all goes good will review and approve if not they will add the comment for changes and change it again rise the pr and review if ok review changes and approve and here we will se "create a  merge commit"
```

#### rebase pull request

- in rebase the commit id's are changed for rebase but in merge extra commit id we will get but in rebase the commit id's are chnaged no extra commit id is created.
- it will not preserve the history
- it will change the commit id's it means it will re-write
- it forms linear structure
- no un-nesesary commit id's

```
again one new feature branch is created so again rise the pr and review it and create pull request and if all goes good will review and approve if not they will add the comment for changes and change it again rise the pr and review if ok review changes and approve and here we will se "rebase and merge"
```
- if u want history go with merge
- if u dont want history go with rebase

#### squash and merge
- combining every thing into one commit id
- if u dont want many commit id's go with squash and rebase
- while developing the feature one feature is developed by one developer we have one week or two week sprints this is micro services he may do lot of commits as part of feature developer if we dont use squash we may get lot of commits so we use squash the commits as part of one feature and mention as one feature commit id is changed 

```
again one new feature branch is created so again rise the pr and review it and create pull request and if all goes good will review and approve if not they will add the comment for changes and change it again rise the pr and review if ok review changes and approve and here we will se "squash and merge"
```
# branching strategy
- we are using master and feature branching startegy master is long lived branch feature is short leaved branch and no one is allowed to do changes directly to the master we should rise pr minumum 3 approvals we need to do changes in master rise pr and get the approval and while merging we choose merge option as our merging strategy and why we choose merge is it will preserve the history as per our project requirement

- why dont you choose rebase?
- in rebase history is not preserved and new commit ids are chnaged the requirement we got is they wants the preserved history.

```
master ----> main -->long leave
feature ---> shortleaved--> we can delete generally in our project will not delete because we are scared 
```

# Trunk based development
- trunk based only one branch is master long live 
- you do changes directly here if we wants to directly we should have lot of checks --> before going to prodouction testing should be done 100% automation we should do unit test,functional testing, automaton testing,all types of scanning
- if we are doing only in one branch we should be perfect we have to know what we are doing and all should be done automation. full metured automation. but we will not use this clients and we are very scared about this

#### merge conflicts
- how you resolve merge conflicts 
if git find different contents from same line it cant take decisison what to take what not to keep
so developers who developed both of then sit together and check what to keep what not to keep so after chaanging then we will aprove and merge. 
