# demo-home-site

- Directory of files used to build https://demo.webwork.rochester.edu/public using Hugo

- Pull requests for improving the information available here are welcome.

- To download and run this on your own computer use the following steps 
(loosely this works for me but there hasn't been much testing yet)

- install hugo ( on a mac I used homebrew) -- there is lots of good webdocumentation https://gohugo.io/getting-started/quick-start/
	- brew install hugo
- Optional: (If you have a git hub account you should fork the demo-home-site to your github account and then clone to your desktop from your own copy of the repos.  That will make it easy to submit pull request changes. If you don't have a github account and don't want to create one you can skip this step.)

	- if you don't already have a github repository go to https://github.com  and create one.
		- it takes less than 5 minutes.  It will ask for an email address and you choose a name for
		  your github site (my name "mgage")
	- sign in to your new github site (your name or picture will appear in the upper right corner if you are
		  signed in.)
	- go to `https://github.com/mgage` and click the tab "repositories" and then on "demo-home-site"
	- in the upper right corner you will see "fork", click on that to make a copy of demo-home-site on
		 your own github account. 
- cd to a directory that will enclose the directory demo-home-site you are about to create and type
- `git clone https://github.com/YOUR_GITHUB_NAME/demo-home-site .` 
                (if you didn't create your own github account use `mgage` for YOUR_GITHUB_NAME )
- cd demo-home-site 
- type `hugo server -D` might work 
	then view in browser at `localhost:1313/public`
- if not: try just.  hugo     This will try to build the permanent webpage and you may see error messages such as missing HTML layouts and so forth. That suggests the ananke theme files are missing. 
	- in that case look at the contents of demo-home-site/themes/ananke (it might be empty which means that the submodule for ananke wasn't pulled down from github)
	- You fix this with
		- `cd themes`
		- `rmdir ananke`
		- `git rm ananke` 
		- `git submodule add https://github.com/budparr/gohugo-theme-ananke.git ananke`
		- (this reloads the ananke theme  -- anyone know how to force this submodule to be moved when cloning? )
	- Now cd to the top level demo-home-site and try hugo server -D again.
			- (see `https://gohugo.io/getting-started/quick-start/` installing ananke theme)

Please add to or modify the instructions so that they are more helpful. You can submit pull requests.

### When you want to submit modifications there is a three step process 

- upload the changes you
have made on your laptop, and then 
- issue a pull request from you github account to the master 
version at github.com/mgage.  
- I'll check the changes and then incorporate them into the master repos.

Up loading changes 
`git push origin my-newchanges`

You'll be able to view them at `https://github.com/YOUR_GITHUB_NAME/demo-home-site`  by choosing the 
branch `my-newchanges`.

There are also GUI apps such as Github  and SourceTree which can help you with moving files
from your laptop to github and back. 
