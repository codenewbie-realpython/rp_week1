# rp_week1
### Real Python: Week 1(0?) Quick and dirty git guide. Drop code here for comment, review, or funsies May 5 - May 12.
======

## Quick and dirty git guide

#### Add to a repo that already exists

I'm going to assume that you still need to create a new folder to house the new repo. And that you're on an Unix-based system. 

1.	Clone the repo
	*	Navigate to where you want to want the repo to live on your computer using the command line
		Mac/Unix CLI guide [here.](https://github.com/0nn0/terminal-mac-cheatsheet/wiki/Terminal-Cheatsheet-for-Mac-(-basics-))
	*	`git clone <<https git address> <<new folder name that will hold the repo on your comp>>`
                The address for cloning is on the sidebar of the repo on GitHub.com. The last argument is optional. If you don't include it, you'll simply add a copy of the folder, named as it is in the repo.
2.	Add/make a folder, and add your code. => `git add` ("Gather items to ship")
        *       Create a new folder with your name and add your code into the folder.
        *       Switch to the terminal, and after making sure you're still in the repo folder (`pwd` to check), type `git add .` You actually have a few options here. Using the period adds all untracked or changed files. If you enter `-i` instead of the period you can use git's interactive command line interface to add files. Otherwise, you can just add individual files by filename, omitting the period and the dash i.
                `git add` is roughly equivalent to making a packing list for the imaginary package you're going to send to the repo.
3.	"Box the items you want to ship" => `git commit`
        *       Once you've git added the folders and files you want to send, they need to be committed.
        *       `git commit -m "<<short description of the changes you're making>>"`
                If you forget or omit the `-m "<<message>>"`, your default text editor will open: likely vim. Don't panic, you can still add both your short message and a longer explanation. If you end up in vim, type `a` to begin typing. The first line is the short message. Add a blank line, and then you can add your long message/description. When you're done. Press `<Esc>`, and then type `:wq` to save and quit.
                The box has now been packed with the things you want to send to the repo and a note describing the contents. 
4.	"Ship the package" => `git push`
        *       Last step is to send the package.
        *       `git push origin master`
                This translates to: "git, push (my committed files) to origin from master. The default name of the remote that we cloned in step 1 is origin, and we are pushing our local master to the remote. Git will ask you for your username and password, and will confirm the push when complete. And that should be it.

Let me know if these directions are unclear or if they don't work for you.
        
