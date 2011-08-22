clockd
======

Clockd provides a simple, easy to use command-line interface for measuring the time you spend on a project.

Convenience of the command line
-------------------------------

For all of you out there who hate to use GUI applications, this is just the tool for you.  Never again will you have to click a button to start a timer, or manually add up a bunch of numbers to figure out how much your next paycheck will be.  With clockd, just clock-in, clock-out, and sum up your time, all with a few simple Terminal commands.

Usage
=====

Clockd tracks your total time working on a project, but also records individual "sessions" of work.  To begin a working session on any project, use the ```start``` sub-command:

    $ clockd start "My Project"
    Working on "My Project"
      beginning at Sun, 21 Aug 11 21:49:19 -0400
       duration: 0:00:00:00

Then, check on your current work status with ```clockd status```

    $ clockd status
    Working on "My Project"
      beginning at Sun, 21 Aug 11 21:49:19 -0400
       duration: 0:00:30:00

Once you are finished working for the day, just clock-out using ```clockd stop```.

    $ clockd stop
    Worked on "My Project" for 0:20:34:12.

Of course, it's always nice to have your computer do math for you.  That's why you can use the ```clockd summary``` command to check out your total hours on all of your projects:

    $ clockd summary
    Worked on My Project for 0:04:23:44.
    Worked on TV for 0:00:30:39.
    Worked on SuperLists for 0:02:57:40.

Installation
============

Clockd requires that you have the PHP Command Line Interface installed somewhere in your ${PATH}.  This is already the case for most versions Linux and Mac OS X.  With this requirement met, simply copy the clockd script to a directory in your path (possibly ```/usr/local/bin```) and enjoy!

    sudo cp ./clockd /usr/local/bin/
    sudo chown root /usr/local/bin/clockd
    sudo chmod 755 /usr/local/bin/clockd
