---
layout: page
title: "Setup"
permalink: /setup/
---

> ## Experienced Python Devs
>
> If you already have a working Python 3 environment, you **do not have to** install
> Anaconda as per the instructions below. We will use Jupyter notebooks for the
> workshop, but you can install them with pip (see the
> [Jupyter website][jupyter-install] for details.) You can install all of the  
> libraries we will be using as follows:
> ~~~
> pip install --upgrade pip
> pip install jupyter pandas pycallnumber
> ~~~
> {: .source}
{: .callout}

## Installing Python Using Anaconda

[Python][python] is a popular language for research computing, and great for general-purpose programming as well. Installing all of its research packages individually can be a bit difficult, so we recommend [Anaconda][anaconda], an all-in-one installer.

Regardless of how you choose to install it, **please make sure you install Python version 3.x** (e.g., 3.6 is fine). Also, please set up your python environment at
least a day in advance of the workshop.  If you encounter problems with the
installation procedure, ask your workshop organizers via e-mail for assistance so
you are ready to go as soon as the workshop begins.

### Windows

1. Open [https://www.anaconda.com/distribution/#windows][anaconda-windows]
   with your web browser.

2. Download the Python 3 installer for Windows.

3. Install Python 3 using all of the defaults for installation _except_ make sure to check
**Add Anaconda to my PATH environment variable**.

### Mac OS X

1. Open [https://www.anaconda.com/distribution/#macos][anaconda-mac]
   with your web browser.

2. Download the Python 3 installer for OS X.

3. Install Python 3 using all of the defaults for installation.

### Linux

Note that the following installation steps require you to work from the shell.
If you run into any difficulties, please request help before the workshop begins.

1.  Open [https://www.anaconda.com/distribution/#linux][anaconda-linux] with your web browser.

2.  Download the Python 3 installer for Linux.

3.  Open a terminal window.

4.  Type

    ~~~
    $ bash Anaconda3-
    ~~~
    {: .bash}

    and press <kbd>Tab</kbd>. The name of the file you just downloaded should appear. If it does not, navigate to the folder where you downloaded the file, for example with:

    ~~~
    $ cd Downloads
    ~~~
    {: .bash}

    Then, try again.

5.  Press <kbd>Return</kbd>. You will follow the text-only prompts. To move through the text, press <kbd>Spacebar</kbd>. Type `yes` and press <kbd>Return</kbd> to approve the license. Press <kbd>Return</kbd> to approve the default location for the files. Type `yes` and press <kbd>Return</kbd> to prepend Anaconda to your `PATH` (this makes the Anaconda distribution the default Python).

6.  Close the terminal window.

## Getting the Data

The data we will be using is sample library data.
To obtain it, download and unzip the file
[library-data.zip][data-zip].
In order to follow the presented material, you should launch a Jupyter
notebook in the "data" directory (see [Starting Python](#Starting-Python)).

## Starting Python

We will teach Python using the [Jupyter notebook][jupyter], a
programming environment that runs in a web browser. Jupyter requires a reasonably
up-to-date browser, preferably a current version of Chrome, Safari, or Firefox
(note that Internet Explorer version 9 and below are *not* supported). If you
installed Python using Anaconda, Jupyter should already be on your system. If
you did not use Anaconda, use the Python package manager pip
(see the [Jupyter website][jupyter-install] for details.)

To start the notebook, open a terminal or git bash and type the command:

~~~
$ jupyter notebook
~~~
{: .bash}

To start the Python interpreter without the notebook, open a terminal
or git bash and type the command:

~~~
$ python
~~~
{: .bash}

[anaconda]: https://www.anaconda.com
[anaconda-mac]: https://www.anaconda.com/distribution/#macos
[anaconda-linux]: https://www.anaconda.com/distribution/#linux
[anaconda-windows]: https://www.anaconda.com/distribution/#windows
[data-zip]: {{site.github.repository_url}}/blob/gh-pages/files/library-data.zip]?raw=true
[jupyter]: http://jupyter.org/
[jupyter-install]: http://jupyter.readthedocs.io/en/latest/install.html#id4
[python]: https://python.org

{% include links.md %}
