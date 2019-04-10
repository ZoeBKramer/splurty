# Install Ruby on Rails

# Set Up Vagrant

Click [here](windows-vagrant.md) to find the instructions for setting up Vagrant.

### Vagrant

Between each of the coding sessions you do, especially if you restart your machine, you will need to run the following command to start your vagrant environment prior to connecting:

`vagrant up`

When this command completes, run the vagrant ssh command to log in to Vagrant.

After this completes, you will be taken to a coding environment inside your virtual machine, and your terminal should contain the green [ENV].

![Vagrant CLI](images/windows-dev-setup-image_0.png)

Running the `killall ruby` command in your terminal should quit all running Rails servers.

**To ensure that your server is not running** -— If you visit the URL [http://localhost:3030](http://localhost:3030) in your browser, you should not see a web page load. You should ensure that your server is not running before starting new server windows.

**If you want to preview the application that is running within your coding environment**—Visiting the [http://localhost:3030](http://localhost:3030) from your web browser will allow you to do this.

**Location of project files**—When using this vagrant environment, most people will store the code for their specific projects in the folder in the location `/vagrant/src` inside their coding environment.

All the files within this folder inside the Vagrant environment will be automatically synced outside the Vagrant environment to folder inside the `coding-environment/src` folder that is located outside the virtual machine, usually on your Desktop.
