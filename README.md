# Installing-Tensorflow (compiled from tensorflow.org and a few other sources)

Install Tensorflow on Ubuntu with virtualenv. This guide is aimed for those with Python 2.7.x installed. To check your python version, write "python" terminal window. You'll see the following line(s):

Python 2.7.12 (default, Jul 20 2017, 18:23:56) 
[GCC 5.4.0 20160609] on linux2
Type "help", "copyright", "credits" or "license" for more information.

# Type exit() to exit the Python command line

# Proceed
# Open terminal and get admin rights
sudo su 

# Install pip and create a virtual environment
sudo apt-get install python-pip python-dev python-virtualenv
virtualenv --system-site-packages ~/tensorflow

# Activate the virtualenv environment
source ~/tensorflow/bin/activate 

# Your prompt will now be changed to:
(tensorflow)$ 

# Tensorflow installed
# When you are done using TensorFlow, you may deactivate the environment by:
(tensorflow)$ deactivate 

# Run a test program
# You'll have to activate your virtualenv environment every time you want to use tensorflow:
source ~/tensorflow/bin/activate 

# Invoke Python and enter the following program
python
import tensorflow as tf
hello = tf.constant('Hello, TensorFlow!')
sess = tf.Session()
print(sess.run(hello))
# The program should output:
Hellow, Tensorflow!


# To uninstall Tensorflow
$ rm -r ~/tensorflow

