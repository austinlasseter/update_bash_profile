# update_bash_profile
Here's that pesky line of code you need when you have to make sure Anaconda runs properly.

On a Windows machine, you can find your machine name here: Control Panel\System and Security\System

from any directory, simply type: vi .bash_profile

Here’s what you need to add to your bash_profile:
``` 
# get the aliases and functions
if [ -f ~/.bashrc ]; then
                . ~/.bashrc
fi

# User-specific environment and startup programs
export DISPLAY=<your computer name>:0.0
PATH=/opt/Anaconda3-5.1.0/bin:$HOME/bin:$PATH
export PATH
```
