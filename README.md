Click [here](https://splurty-zoe-kramer.herokuapp.com/) to visit Splurty. 

# Set Up Vagrant

Click [here](https://github.com/university-bootcamp/coding-environment/blob/master/windows-vagrant.md) to find the instructions for setting up Vagrant.

### Vagrant

Between each of the coding sessions you do, especially if you restart your machine, you will need to run the following command to start your vagrant environment prior to connecting:

`vagrant up`

When this command completes, run the vagrant ssh command to log in to Vagrant.

After this completes, you will be taken to a coding environment inside your virtual machine, and your terminal should contain the green [ENV].

Running the `killall ruby` command in your terminal should quit all running Rails servers.

**To ensure that your server is not running** -— If you visit the URL [http://localhost:3030](http://localhost:3030) in your browser, you should not see a web page load. You should ensure that your server is not running before starting new server windows.

**If you want to preview the application that is running within your coding environment**—Visiting the [http://localhost:3030](http://localhost:3030) from your web browser will allow you to do this.

All the files within this folder inside the Vagrant environment will be automatically synced outside the Vagrant environment to folder inside the `coding-environment/src` folder that is located outside the virtual machine, usually on your Desktop.

# Set Up Splurty

### Checking Out the Repo

Check this repository out into your `coding-environment/src` folder. 

### Create the Initial Database

Connect to your Vagrant instance, change the directory `cd /vagrant/src/splurty`

Run `rake db:create`

### Starting Up Your Server

In a separate terminal, change the directory `cd /vagrant/src/splurty`

Start your server by running `rails server -b 0.0.0.0 -p 3000`

# Splurty

### Overview

A web application, built with Ruby on Rails, that allows users to enter a quote followed by the author. The quotes are stored into the database using Postgresql. These quotes are then outputted randomly onto the front page. 

### Code Structure

**Web App Layout** - On each page in the web application, the header and the footer are present. You can find the code for this in `app\views\layouts\application.html.erb'.

**Index Page** - This is where all of the quotes are outputted at random. This is happening inside of the `app\controllers\quotes_controller.rb` file, within the index method. The view for this page is in `app\views\quotes\index.html.erb`. 

**About Page** - This page can be found in `app\views\quotes\about.html.erb`. 

**Creating a Quote** - The method for adding a new quote into the database is found in the `app\controllers\quotes_controller.rb` file, within the create method. The modal form for adding said quote can be located in `app\views\quotes\new.html.erb`. 
