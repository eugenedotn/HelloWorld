<h3>Prerequisites for HelloWorld app:</h3>

<p>The app has been tested on Arch Linux, so there will only be OS-specific commands for packages' installation.
So to get started you will need to get Vagrant installed.</p>
For Arch just run:

<code> **sudo pacman** -S vagrant </code>

pacman will also install all of the dependencies for vagrant.
After that you need to get the Ansible installed: 

<code> **sudo pacman** -S community/ansible </code>

Same, basically, goes for ansible - pacman will add all of the dependencies for it.

Once that is done all you will need to do is to checkout the app from the GitHub to your local machine:

Create the directory for the project:

<code> **mkdir** {dir_name}</code>

<code> **cd** {dir_name} </code>

Initialize the git environement there and add remote repo:

<code> **git** init </code>

<code> **git** remote add https://github.com/eugenedotn/HelloWorld.git </code>

Next pull it to master brach (or whatever you want to call it):

<code> **git** pull origin master </code>

Once it is done you need to run one simple command to get your stack deployed:

<code> **vagrant up** </code>
<code> **vagrant ssh python </code> will SSH you into the app VM while <code> vagrant ssh nginx </code> will log you into the NGINX web-server VM.

You will be able to access the newly deployed Helloworld app locally in your browser by navigating to http://localhost:8080
