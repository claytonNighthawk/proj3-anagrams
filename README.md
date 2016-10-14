# proj3-anagrams
Vocabularly anagrams game for primary school English language learners (ELL)

### What do I need?  Where will it work? ###

* Designed for Unix, mostly interoperable on Linux (Ubuntu) or MacOS.
  Target environment is Raspberry Pi. 
  ** May also work on Windows (at least the W10 Ubuntu bash) or a Linux virtual machine
   out of the box depending on your pyvenv package command name. Program might require manual configuration with `. env/bin/activate`, `make configure` and `pip install -r requirements.txt` or changing the PYVENV command name in templates.d/Makefile.standard between pyvenv and virtualenv. I could not get "pyvenv" to install on my pi or anywhere else but virtualenv worked everywhere.    
   
* You will also need Python version 3.4 or higher. 
* Designed to work in "user mode" (unprivileged), therefore using a port 
  number above 1000 (rather than port 80 that a privileged web server would use)

## In your workspace

`bash ./configure` or `make run` should create appropriate configuration files on
most Unix files.   If you are using Windows, some additional editing
of configuration files may be necessary (similar to what was mentioned above).  You might have to edit the
Makefile to find the right version of pyvenv.

If you can run flask applications in your development environment, the
application would might be run by
`   python3 flask_vocab.py` or `make run`
and then reached with url
`   http://localhost:5000`

## Overview

A simple anagram game designed for English-language learning students in 
elementary and middle school.  
Students are presented with a list of vocabulary words (taken from a text file) 
and an anagram.  The anagram is a jumble of some number of vocabulary words, randomly chosen.  Students attempt to type vocabularly words that can be created from the  
jumble.  When a matching word is typed, it is added to a list of solved words. 

The vocabulary word list is fixed for one invocation of the server, so multiple
students connected to the same server will see the same vocabulary list but may 
have different anagrams.

## Authors 

Initial version by M Young; Revised by Clayton Kilmer, kilmer@cs.uoregon.edu 

## To run automated tests 
* `nosetests`

There are currently nose tests for vocab.py, letterbag.py, and jumble.py. 



