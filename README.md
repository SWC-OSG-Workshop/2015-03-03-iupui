============================
#Software Carpentry - Open Science Grid (SWC-OSG) Workshop#
============================

We work directly on the `gh-pages` as it is useful for the website 
rendering. GitHub renders the website from the HTML and markdown 
files kept under `gh-pages`. For example, the HTML and 
markdown files of this branch are rendered at the url: 
CurrentWebPage (http://SWC-OSG-Workshop.github.io/2015-01-03-iupui ). 
displayed on the webpage and available to the participants, we want to directly work 
on `gh-pages`. This is the standard practice recomended by the software carpentry. 


The `gh-pages` branch contains the basic learning modules and necessary 
tools to set up new websites for the up-comping worshops. In this repo, we will 
update all the new materials and make generic changes to the woskshop front page. 


The sections below explain:

* __How to set up the git repo on your local machine.__
* __How do we edit the course materails.__
* __How do we edit the workshop front page.__


**Table of Contents**

*   [Getting Started](#getting-started)
*   [Lesson Material](#lession-material)
*   [Workshop Front Page](#workshop-frontpage)

##Getting Started##
---------------


Now let us see how to make a copy of the existing repo on your locale machine.  In your local 
desktop or laptop, clone the repo 

~~~
     git clone https://github.com/SWC-OSG-Workshop/2015-01-03-iupui.git
~~~

and create new branch named `gh-pages`.

~~~
     git checkout -b gh-pages
~~~

Now pull the content repository's `gh-pages` branch into your desktop repository:

~~~
     git pull origin gh-pages
~~~
##Lesson Material##
---------------

The current material is in the directories under `novice`. The shell and Git materials are 
written in Markdown, while the Python and SQL use the IPython Notebook. 

The material related to OSG is in the directory `novice/DHTC` and are written in Markdown.  Once 
finished editing the material at `novice/DHTC/filename.md`, push the content to the repository:

~~~
     git add filename.md
     git commit -m "some message here about the changes " 
     git push origin gh-pages
~~~



##Workshop Front Page##
-------------------

Editing workshop front page involves editing html pages. Two html files are of 
primary interest to us. One is the "index.html" and other is "_includes/setup.html".


Edit `index.html` to make any changes to the workshop home page.
    In particular, the variables such as venue, date etc., in the page's header,
    as these are used to update the main website, and make sure the website-content is correct.
    You can use the script `./bin/swc_index_validator.py` to 
    check `index.html` for problems
    by running the command `make check`.


Edit `_includes/setup.html` to provide software installation instructions for the workshop attendees.

Once finished editing the index.html, push content to the repository:
~~~
     git add index.html
     git commit -m "some message here about the changes " 
     git push origin gh-pages
~~~

As soon as the repo has been pushed to GitHub, GitHub will render the pages
at the URL http://SWC-OSG-Workshop/2015-01-03-iupui 

