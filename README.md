# Week 9 - Deep Learning

Welcome to week 9 of the Data Science Immersive course. Over the next week we'll cover one of the most exciting family of algorithms: Deep Learning.

## Repository

The course material for Deep Learning can be found [here](https://github.com/misk-data-science/misk-dl). We'll explore setting up cloud computing once we want to explore more advanced modelling, the course material for that section can be found [here](http://scavetta.academy/misk/mlops/0_main.html). 

## Additional materials for your Capstone Project

For those of you intersted in exploring Natural Language Processing the course material can be found [here](http://scavetta.academy/misk/nlp/0_main.html).

## Setting up your AMI for cloud computing


1. Make sure you have an account at Amazon Web Services.

1. Make sure you have set up a payment method in the billing section.

1. Go to the marketplace, and install the [RStudio Tensorflow GPU](https://aws.amazon.com/marketplace/pp/B0785SXYB2?ref_=srh_res_product_title)

1. Click on "continue to subscribe"1. On the next page, click on "continue to Configuration"

1. On the next page, choose the region that is closest to you or that matches with your account. If there is a mismatch you will have to wait a few hours until it is resolved, so pay attention to the error messages you will get here.
1. On the next page, "Launch this software", scroll to the bottom and make sure that you have a Key Pair selected in the "Key Pair Settings" box. If you don't select the "Create a key pair in EC2" link and make a Key Pair in that tab. Use a `.pem` file. Come back and refresh the pulldown menu and choose your Key Pair. You can also do this at the very end.

1. Return to the top of the page and choose "Launch from EC2". This will allow you to use all the default setting for your instance instead of setting them here. Your "launch" button should be orange and ready to go.

1. On the next page, click on "Review and Launch".
1. On the next page, click on "Launch".

1. In the pop-up window, choose the Key Pair that you made earlier and check the check box. Click "launch instances".

1. On the next page, while your instance in initializing, you can view your instance in a list by clicking on "View Instances". On the next page your instance will appear at the bottom of the list and be labeled at "initializing..."

1. Click on the name "-" to change it to something meaningful.

1. Click on the Instance ID to see the information. Here you can find the usage instructions. 

1. You'll also find the instance's public DNS location. It will look something like: `ec2-11-111-111-11.eu-central-1.compute.amazonaws.com`. To use this use your browser to go to `http://<your DNS>:8787`. 

1. To log into your account, use the username `rstudio-user` and your instance id as the password. Your instance id will look something like this: `i-11f111c11bcaf4111`.

1. Follow the instructions in the usage instruction to check that tensorflow is installed and working:

1. Once logged in, please set a new password for this user:
* Click the "Tools" menu dropdown
* select "shell"
* type "passwd" into the shell
* enter the current password (instance_id) and the new password twice, hitting the enter key after each entry.

1. Begin using tensorflow-related tooling in R to make use of the GPU: The following is recommended but may not work. Try to clone our project in the next step:
* library(tensorflow)
* sess = tf$Session()
* Accept the option to insall Anaconda
* run `install_tensoflor(version = "gpu")`
* hello <- tf$constant('Hello, TensorFlow!')
* sess$run(hello)

1. Set up a new project from GitHub and clone the repo for the DL material: `https://github.com/misk-data-science/misk-dl`.
