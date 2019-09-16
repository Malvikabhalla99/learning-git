Learning git commands

Various situations in which you may use git and github

1. Creating a standalone repo on github and just adding your project to it
2. Created a repo and frequently updating the project or just adding your code to a branch
3. Working on a repo in which your are a collaborator and updating your branch frequently and opening pull requests
4. Working on a repo in which you are not a collaborator and created your own copy and opened a pull request


Various ways to implement these 

1. Creating a standalone repo on github and just adding your project to it
	Create a repo on github
	Note - Don't create a readme at that time
	Write the following commands on the terminal
		Go to the project directory using cd 
		git init
		git add . 
		git commit -m  "Added Readme"
		git remote add origin <url of your repo>
		git remote -v
		git push -u origin master
		
2. Created a repo and frequently updating the project or just adding your code to a branch
	Create a repo on github
	Note - Don't create a readme at that time
	Write the following commands on the terminal
		Go to the project directory using cd 
		git init
		Create a readme file 
		git add readme
		git commit -m "Initial commit"
	Create a new branch on github eg abc 
	git fetch --all
	git branch -a
	'''
	now you will be able to see the newly created branch
	In the above case you would created a new branch by cutting it from master  
	If you are cutting a new branch from any other branch then ensure that you are on the same branch from which you have cut the new branch
	For eg if abc is cut from master then on terminal be on master branch 
	Similarly if you have cut the branch from xyz then be on branch xyz in terminal
	If you haven't created the branch xyz ,then first track xyz 
	'''
		Tracking xyz , being on master branch
		git checkout -b xyz
		git branch --set-upstream-to origin/xyz
		git pull origin xyz --allow-unrelated-histories
		
	'''creating a new branch abc being on the correct branch in terminal '''
	git checkout -b xyz
	git branch --set-upstream-to origin/xyz
	git pull origin xyz --allow-unrelated-histories
	
	'''Make changes in your directory , add your code or update the existing files'''
	git status
	git add . 
	git commit -m "Commit message"
	git push 
	

		
		
		
