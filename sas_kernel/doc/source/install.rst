
.. Copyright SAS Institute


=========================
Installing the SAS kernel
=========================

The SAS kernel package installs just like any other Python package.
It is a pure Python package and works with Python 3.X
installations.  To install using ``pip``, you execute one of the
following commands.

::

    pip install sas_kernel
    pip install http://github.com/sassoftware/sas_kernel/releases/sas_kernel-X.X.X.tar.gz


******************************************************************
Linux install for Anaconda Python (assuming SAS already installed)
******************************************************************

#. Go to https://www.continuum.io/downloads and install
   Anaconda Python (make sure you get Python3.X). If you install
   Anaconda without Superuser privileges (root or sudo), then other users
   on the system will not be able to access the SAS kernel. Consider the
   following:

   * The default installation location is your home directory. This is
     fine for a single user install. If you want a system-wide installation,
     then use a common location such as ``/opt``.

   * One installation prompt is to add the path to your environment. SAS
     recommends that you answer 'yes' to the prompt so that you get the
     executables in your path automatically. If you are performing a system-wide
     installation (using root or sudo), then all the other users must add
     the path to their environmental variables.

#. Install the SAS kernel package. The package has a dependency on the SASPy
   package. The SASPy package is available from https://github.com/sassoftware/saspy.
   If the ``pip`` command in your path does not map to Python3, then use ``pip3``
   instead.
   ::

       pip install sas_kernel

#. Verify that the package is installed.
   ::

       jupyter kernelspec list

   If you installed as a Superuser, your output should look similar to the following:
   ::

       Available kernels:
         python3    /opt/Anaconda3-2.5.0/lib/python3.5/site-packages/ipykernel/resources
         sas        /usr/local/share/jupyter/kernels/sas

   If you installed as a regular user (the sas user account, in this case), your output
   should look similar to the following:
   ::

       Available kernels:
         python3    /home/sas/anaconda3/lib/python3.5/site-packages/ipykernel/resources
         sas        /home/sas/.local/share/jupyter/kernels/sas

#. Configure the SAS executable for your system.

   The connection of the Jupyter notebook to SAS is made by the SASPy Python package (which was installed as a dependency
   for you).


   Use the `SASPy configuration documentation`_ to complete you set up.

   .. _SASPy configuration documentation: https://sassoftware.github.io/saspy/configuration.html

   * SASPy documentation: https://sassoftware.github.io/saspy/index.html
   * More information about SASPy: https://github.com/sassoftware/saspy


***********************************************************
Linux install for Centos 6 (assuming SAS already installed)
***********************************************************

These instructions describe hot to perform a system-wide installation for all users.
You must have Superuser privileges (root or sudo).

#. You can use the ``yum`` command to install from RPM packages.
   ::

     sudo yum install https://centos6.iuscommunity.org/ius-release.rpm
     sudo yum install python35u gcc-c++ python35u-devel python35u-pip python35u-tools

#. You can use the ``pip`` command.
   ::

     wget https://bootstrap.pypa.io/get-pip.py
     python3.5 get-pip.py
     pip3 --version``

#. Install Jupyter and the SAS kernel package. The package has a dependency on the SASPy
   package. The SASPy package is available from https://github.com/sassoftware/saspy.
   ::

     pip3.5 install jupyter
     pip3.5 install sas_kernel

#. Verify that the SAS kernel package is installed.
   ::

     jupyter kernelspec list

   Your output should look similar to the following:
   ::

       Available kernels:
         python3    /usr/lib/python3.5/site-packages/ipykernel/resources
         sas        /usr/local/share/jupyter/kernels/sas

#. Configure the SAS executable for your system.

   The connection of the Jupyter notebook to SAS is made by the SASPy Python package (which was installed as a dependency
   for you).


   Use the `SASPy configuration documentation`_ to complete you set up.

   .. _SASPy configuration documentation: https://sassoftware.github.io/saspy/configuration.html

   * SASPy documentation: https://sassoftware.github.io/saspy/index.html
   * More information about SASPy: https://github.com/sassoftware/saspy


************************************************
Windows install (assuming SAS already installed)
************************************************

#. Go to https://www.continuum.io/downloads and install
   Anaconda Python (make sure you get Python3.X). If you install
   Anaconda without Administrator privileges, then other users
   on the system will not be able to access the SAS kernel. Consider the
   following:

   * Install in the default location unless you have a good reason to change it.
     Using the default location simplifies administration.

     .. image:: ./images/ap3.PNG
        :scale: 50%

   * One installation prompt is to make Python accessible for just your account
     or for all users.  Select the best response for your situation.

     .. image:: ./images/ap2.PNG
        :scale: 50%

   * Another installation prompt is to add the path to your environment. SAS
     recommends that you answer 'yes' to the prompt so that you get the
     executables in your path automatically. Adding the path your environment
     simplifies starting Python and Jupyter.

     .. image:: ./images/ap4.PNG
        :scale: 50%


   .. IMPORTANT::

      This next group of steps is performed from a Windows command prompt (
      :menuselection:`Start --> Run --> cmd`)

#. Install the SAS kernel package. The package has a dependency on the SASPy
   package. The SASPy package is available from https://github.com/sassoftware/saspy.
   If the ``pip`` command in your path does not map to Python3, then use ``pip3``
   instead.
   ::

       pip install sas_kernel

#. Verify that the package is installed.
   ::

       jupyter kernelspec list

   Your output should look similar to the following:
   ::

       Available kernels:
         python3    C:\Users\sas\AppData\Local\Continuum\Anaconda3\lib\site-packages\ipykernel\resources
         sas        C:\ProgramData\jupyter\kernels\sas

#. Configure the SAS executable for your system.

   The connection of the Jupyter notebook to SAS is made by the SASPy Python package (which was installed as a dependency
   for you).


   Use the `SASPy configuration documentation`_ to complete you set up.

   .. _SASPy configuration documentation: https://sassoftware.github.io/saspy/configuration.html

   * SASPy documentation: https://sassoftware.github.io/saspy/index.html
   * More information about SASPy: https://github.com/sassoftware/saspy



*****************
OSX (Mac) install
*****************

#. Go to https://www.continuum.io/downloads and install
   Anaconda Python (make sure you get Python3.X). If you install
   Anaconda without Administrator privileges, then other users
   on the system will not be able to access the SAS kernel. Consider the
   following:

   * Install in the default location unless you have a good reason to change it.
     Using the default location simplifies administration.

   * One installation prompt is to make Python accessible for just your account
     or for all users.  Select the best response for your situation.

   * Another installation prompt is to add the path to your environment. SAS
     recommends that you answer 'yes' to the prompt so that you get the
     executables in your path automatically. Adding the path your environment
     simplifies starting Python and Jupyter.

#. Install the SAS kernel package. The package has a dependency on the SASPy
   package. The SASPy package is available from https://github.com/sassoftware/saspy.
   If the ``pip`` command in your path does not map to Python3, then use ``pip3``
   instead.
   ::

       pip install sas_kernel

#. Verify that the package is installed.
   ::

       jupyter kernelspec list

   Your output should look similar to the following:
   ::

       Available kernels:
          python3              /Users/sas/anaconda3/lib/python3.5/site-packages/ipykernel/resources
          sas                  /usr/local/share/jupyter/kernels/sas


#. Configure the SAS executable for your system.

   The connection of the Jupyter notebook to SAS is made by the SASPy Python package (which was installed as a dependency
   for you).


   Use the `SASPy configuration documentation`_ to complete you set up.

   .. _SASPy configuration documentation: https://sassoftware.github.io/saspy/configuration.html

   * SASPy documentation: https://sassoftware.github.io/saspy/index.html
   * More information about SASPy: https://github.com/sassoftware/saspy


===========================
Installing SAS NBextensions
===========================

********************
Installing from PyPi
********************

With the release of Jupyter 4.2 (SAS kernel package version 1.2) the
installation and enabling of nbextensions is improved. To install and
enable the showSASLog extension use the following commands.

::

    jupyter nbextension install --py sas_kernel.showSASLog
    jupyter nbextension enable sas_kernel.showSASLog --py

To install and enable the theme extension use the following commands.

::

    jupyter nbextension install --py sas_kernel.theme
    jupyter nbextension enable sas_kernel.theme --py

To verify the nbextensions that you installed use the following commands.

::

    jupyter nbextension list

If the extensions are correctly installed, you will see output similar to
the following:

::

    Known nbextensions:
      config dir: /root/.jupyter/nbconfig
        notebook section
          showSASLog/main  enabled
          - Validating: OK
          theme/theme_selector  enabled
          - Validating: OK

***********************************
Installing from a cloned repository
***********************************

The cloned repository has a directory for each nbextension within the
file structure as shown below:

::

    sas_kernel
    |
    +-- showSASLog
    +-- theme

You can install the extensions from the command line. To install an extension
system-wide, use the following command with Superuser privileges (root or
sudo). The following command assumes that you are in the nbextensions
directory. Adjust the path if you are not.

::

    jupyter nbextension install ./showSASLog

Your output should look similar to the following (installed with Superuser
privileges):

::

    copying showSASLog/main.js -> /usr/local/share/jupyter/nbextensions/main.js

To install for your user account only, use the following command. Again,
the sample command assumes that you are in the nbextensions directory. Adjust
the path if you are not.

::

    jupyter nbextension install ./showSASLog --user

Your output should look similar to the following (installed for your user
account only):

::

    copying showSASLog/main.js -> /home/sas/.local/share/jupyter/nbextensions/showSASLog/main.js

Then enable the notebook extension with the following command.

::

    jupyter nbextension enable showSASLog

To disable the extension, you can run the following command.

::

    jupyter nbextension disable showSASLog

Example
=======

There is a `notebook`_ that walks through the steps to install and
enable the extensions.

.. _notebook: https://github.com/sassoftware/sas_kernel/blob/master/notebook/loadSASExtensions.ipynb
