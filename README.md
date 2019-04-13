Click [here](https://splurty-zoe-kramer.herokuapp.com/) to visit Splurty. 

# Splurty

### Overview

A web application, built with Ruby on Rails, that allows users to enter a quote followed by the author. The quotes are stored into the database using Postgresql. These quotes are then outputted randomly onto the front page. 

### Code Structure

**Models** - The splurty app only has one model, the quote model. This handles all the validations for the quote and prevents users from entering blank data. Click [here](https://github.com/ZoeBKramer/splurty/blob/master/app/models/quote.rb) to view this file. 

**Views** - 

*New Quote View*: This is found in [`app\views\quotes\new.html.erb`](https://github.com/ZoeBKramer/splurty/blob/master/app/views/quotes/new.html.erb). This creates the form that the user can enter a quote into.  

*Index View*: This is found in [`app\views\quotes\index.html.erb`](https://github.com/ZoeBKramer/splurty/blob/master/app/views/quotes/index.html.erb). This is what displays a quote from the database onto the screen. 

*About View*: This is found in [`app\views\quotes\about.html.erb`](https://github.com/ZoeBKramer/splurty/blob/master/app/views/quotes/about.html.erb). This controls what is displayed in the 'About Me' section in the app. 

*Header and Footer*: This is found in [`app\views\layouts\application.html.erb`](https://github.com/ZoeBKramer/splurty/blob/master/app/views/layouts/application.html.erb). This controls what is displayed in the header and footer on every page in the application. 

**Controllers** - [`app\controllers\quotes_controller.rb`](https://github.com/ZoeBKramer/splurty/blob/master/app/controllers/quotes_controller.rb). 

*index method*: This method displays a random quote from the database onto the index page.

*create method*: This method adds a new quote (provided that it is valid) into the database. 

**Gemfiles** - This app utilizes the [bootstrap gem](https://github.com/twbs/bootstrap-rubygem) to help format the page. It also uses the [simple-form gem](https://github.com/plataformatec/simple_form) to create the form for the quotes to be entered into. 

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


