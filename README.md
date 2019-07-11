# demo-home-site
Directory of files used to build demo.webwork.rochester.edu using Hugo

Directory of files used to build https://demo.webwork.rochester.edu/public using Hugo

Pull requests for improving the information availabe here are welcome.

To download and run this on your own computer use the following steps (loosely this works for me but there hasn't been much testing yet)

- install hugo ( on a mac I used homebrew) -- there is lots of good webdocumentation https://gohugo.io/getting-started/quick-start/
	- brew install hugo
	
- cd to a directory that will enclose the directory demo-home-site you are about to create
- `git clone https://github.com/mgage/demo-home-site . `  
(If you have a git hub account you should fork the demo-home-site to your github account and then clone to your desktop from your own copy of the repos.  That will make it easy to submit pull request changes. )
- cd demo-home-site 
- hugo server -D might work (view in browser at localhost:1313/public
- if not: try just.  hugo     This will try to build the permanent webpage and you may see error messages such as missing HTML layouts and so forth. That suggests the ananke theme files are missing. 
	- in that case look at the contents of demo-home-site/themes/ananke (it might be empty which means that the submodule for ananke wasn't pulled down from github)
	- You fix this with
		- cd themes
		- rmdir ananke
		- git rm ananke 
		- git submodule add https://github.com/budparr/gohugo-theme-ananke.git ananke
	- Now cd to the top level demo-home-site and try hugo server -D again.
			- (see https://gohugo.io/getting-started/quick-start/ installing ananke theme)

Please add to or modify the instructions so that they are more helpful. You can submit pull requests.
