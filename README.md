Hello World, I have now ssh'd into this repository from my linux terminal!

I set up my system so I can seamlessly access both my school GitHub and 
personal GitHub accounts at the same time. This setup allows me to make 
changes to repositories using their respective usernames and emails 
without any conflict.

To achieve this, I customized my global .gitconfig file by adding 
conditional includes for different directories::

	[includeIf "gitdir:~/personal/"]
	     path = ~/.gitconfig-personal
	 
	 [includeIf "gitdir:~/school/"]
	     path = ~/.gitconfig-school

With this configuration, Git automatically applies account-specific 
settings (like username and email) based on the directory of the repository 
I'm working in. To make it work, I also created supplementary .gitconfig-personal 
and .gitconfig-school files containing the login information for each account.

This way, I can easily manage repositories for both accounts without 
switching settings manually.
