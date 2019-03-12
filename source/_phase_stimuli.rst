Stimuli
=======

Stimuli for each phase are configured on the *Stimuli* tab:

.. figure:: figures/h2-stimulisettings.png
   :align: center
   :height: 400px
   
   The *Stimuli* tab for a specific phase in the *Experiment Editor* dialog. 
   
This tab displays a list of configured *stimuli* and a list of configured *orders*. In this context, 
we use the term *stimulus* to refer to the combination of video (either still images or movies) and
and audio (either standalone audio files, or the audio track taken from a movie file). An *order* is a 
specific ordering of the configured stimuli that can be used when the experiment is run. You must configure
at least one stimulus for a phase, but it is not necessary to configure any orders. 

A display widget (or two, if your experiment is configured for dual stimuli) shows the selected stimulus. 

An option exists to import stimuli for a phase. The format of the import file is described below. 

Configuring Stimuli
-------------------

Stimuli for a phase are configured by clicking the "New" button next to the stimuli list for the phase. 
An existing stimulus can be modified by selecting the stimulus in the list and clicking "Edit", and a
stimulus may be removed from the list by selecting the stimulus and clicking "Remove". 

When creating a stimulus, or editing an existing stimulus, the dialog contents will depend on whether the 
experiment is configured to use one or two screens, and whether or not independent sound stimuli are to be
used. 

.. figure:: figures/h2-create-stimulus-single.png
   :align: center
   :height: 200px
   
   Dialog for experiments configured for a single stimulus and no independent sound stimuli. 
   
.. figure:: figures/h2-create-stimulus-dual.png
   :align: center
   :height: 200px
   
   Dialog for experiments configured for a dual stimuli and no independent sound stimuli. 
   
.. figure:: figures/h2-create-stimulus-single-iss.png
   :align: center
   :height: 200px
   
   Dialog for experiments configured for a single stimulus and independent sound stimuli. 

Each stimulus type has a button to browse and select a file from the local filesystem (or a network drive
accessible from the local machine). A volume slider allows you to set the volume to be used for the stimulus
(if the stimulus does not have sound this is ignored). 

If the "Loop" checkbox is checked, then the stimulus will play to the end and repeat until the trial ends. This
checkbox has no effect for still images. A movie file will play to the end and freeze on its last frame if the 
"Loop" checkbox is checked and the trial runs for longer than the play time of the video. 

An option also exists to display only the configured background color, with no stimulus image, if the "Background
only" checkbox is checked. 

The Stimulus Root Directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Habit preferences dialog has a setting for the folder to be used as the *Stimulus Root*. 
This setting can be useful when sharing or moving 
Habit experiments (or entire workspaces) between different computers. 

.. note:: If you are *creating* and *configuring* experiments on the same computer that you will use to 
   *run* the experiments, then the value of the *Stimulus Root* doesn't matter. Your stimulus files will
   always be found (as long as the files themselves remain in the same location), and you don't need to
   change the *Stimulus Root*. 
   
When you select a stimulus file as described above, Habit compares the file path to the current value of the 
*Stimulus Root*. If the file path is within the folder (or in a subfolder in the hierarchy *beneath* the root
folder), then Habit stores only the portion of the file path *after, or below, the root folder itself*. In all 
other cases, Habit stores the full path to the stimulus file.

.. figure:: figures/h2-preferences.png
   :align: center
   :height: 300px
   
   The *Preferences* dialog can be used to configure the *Stimulus Root Dir*. 

Once a stimulus file is saved using a path relative to the *Stimulus Root*, Habit will always look for the file
using the currently configured root dir. There are two important things to remember about the *Stimulus Root* 
folder 

* the value you specify in the *Preferences* dialog is saved on the computer where Habit is running
* the value is unique to the *Workspace* that you are working in. Different workspaces on the same computer
  can have different values for the *Stimulus Root*. 

If you move an experiment from one computer (or workspace) to another, or if you 
modify the *Stimulus Root Dir* for the workspace where the experiment resides, then Habit may not be able to 
find the stimulus file at the location that was saved for it. 

.. note:: Habit will display stimuli names with a yellow background if any of the configured files cannot be found
   on the local filesystem. This can happen if the experiment configuration was moved from one machine to another (either
   by moving the entire workspace, or by exporting the configuration and importing the experiment on another machine), 
   and the stimuli files are not found at the stored file paths. 

Using the Default Stim Root
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Each time Habit creates a new workspace, it creates a folder called *stim* inside that workspace. When you select the 
*Default Stimulus Root*, Habit uses this *stim* folder within the workspace as its stimulus root. When you use this root, 
you can put all your stimuli into the *stim* folder in your workspace (or into a folder hierarchy below that folder), and
the locations of all stimuli will be saved as locations relative to that root folder. 

Setting up your Habit workspace like this - using the *Default Stimulus Root* - means that you can treat your Habit workspace
folder as a self-contained entity. Moving the entire workspace to another location (either on the same computer, or on another
computer), means that all you need to do on the target computer is to ensure that the *Stimulus Root* is set to the default for 
that workspace.  

Using a shared network folder as the *Stimulus Root*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In a lab where a user may develop an experiment while working on one computer (their own laptop, for example), but will later *run* the 
experiments on a *different* computer, the configuration of the workspace and the *Stimulus Root* (and, consequently, 
the paths stored for the various stimulus files) is important. 

There are several ways to ensure that the stimulus files are found when running Habit on either computer in this scenario. Here are two 
such methods:

1. Create the workspace in a shared network location, and use the *Default Stimulus Root*. In this case, Habit will store
   relative locations for the stimuli files *within the default stim folder*. On each computer that accesses this shared 
   workspace location, the *Default* stimulus root should be chosen in the *Preferences* for that workspace. Remember, the 
   settings in the *Preferences* dialog are saved on a per-computer, per-workspace basis. Since the file path to the workspace
   itself will vary from computer to computer (because it is in a network path, the actual path from various computers can be 
   different). 
2. Create the workspace on the local computer, but set up a shared network location as the *Default Stimulus Root*. This may be
   a convenience for a lab that has a large collection of stimulus files that are shared across multiple experiments, or 
   chooses to consolidate their stimulus files in a central location for some other reason. Under this scenario, an experiment
   configured using the shared network location as its *Stimulus Root* can be exported and moved to another computer. On the 
   target computer, import the experiment into a workspace and set the *Stimulus Root* to the same network location. Similarly, 
   the entire workspace may be moved to another computer, and the *Stimulus Root* should be set on the target computer after
   opening the workspace. 

Configuring Stimuli Orders
--------------------------

Stimuli orders may be configured for a phase once you have some stimuli configured (see above). To create a new order, click
"New" button next to the stimuli order list for the phase. 
An existing stimulus order can be modified by selecting the stimulus in the list and clicking "Edit", and a
stimulus order may be removed from the list by selecting the order's name and clicking "Remove". 

.. figure:: figures/h2-stimulus-orders.png
   :align: center
   :height: 300px
   
   Stimulus orders are created and modified using this dialog. Individual stimuli are added to the order by selecting them and
   clicking the ">>" button (similarly, they are removed from an order by clicking the "<<" button), or by double-clicking 
   the stimulus name in the "Available Stimuli" list. Stimuli may be moved up or down in the order by selecting the stimulus name
   in the "Stimulus Order" list and clicking either "Move Up" or "Move Down".
   
 
Importing Stimuli/Orders
------------------------

Stimuli and/or stimuli orders for a phase may be imported from a text file. This can be useful for experiments with many stimuli
and for which suitably randomized ordering across subjects is desirable. 

.. figure:: figures/h2-import-stim.png
   :align: center
   :height: 300px
   
   To import a file, click the **Import** button on the *Stimuli* tab for the phase. 

The text file to import may have stimuli, stimuli orders, or both. The stimuli and orders can be in any order. All imported
stimuli and orders are *appended* to existing stimuli and orders. 

Any lines that are blank, or that begin with #, are ignored. 

Specifying a stimulus
~~~~~~~~~~~~~~~~~~~~~

A single stimulus (which specified the stimuli on each monitor and an independent sound file, if any) 
is specified on a single line. The general format of a line containing a stimulus is ::

   stim,<stim-name>,<stim-position-1>,<stim-filename-1>,<stim-position-2>,<stim-filename-2>,...
   
Note that the fields are separated by commas; spaces are trimmed from the start and end of each field. Fields with 
embedded spaces should be enclosed in double quotes, e.g. \"My stimuli\". The fields and their contents are:

*stim*
   The word "stim" indicates that this line contains a stimulus. 
   
*<stim-name>*
   Replace this with the name assigned to the stimulus. The name must be unique among the stimuli for this phase.

*<stim-position-n>*
   Replace this with the *position* for the stim. *Position* can be *right*, *left*, *center*, *sound*, or *audio*. 

*<stim-filename-n>*
   Replace this with the filename for the stim at position *<stim-position-n>*. The filename can be a full path (i.e. 
   a path beginning with \"/\" on Mac/linux, or beginning with a drive letter on Windows), or a relative path (it will be 
   appended to the *Stimulus Root Folder*) 
   

Below is an example taken from the file *\"ross-sheehy.csv\"*, which was used to import the stimuli for the 
*RossSheehy* template experiment. The experiment uses two monitors and no sound files. ::

   stim,stim-letters-plants-1,left,examples/images/letters/A.jpg,right,examples/images/plants/alumroot.jpg,,
   stim,stim-letters-plants-2,left,examples/images/letters/B.jpg,right,examples/images/plants/butterflyweed.jpg,,
   stim,stim-letters-plants-3,left,examples/images/letters/C.jpg,right,examples/images/plants/chamomile.jpg,,

.. Note::

   You cannot specify a volume level, or check the "Loop" checkbox, with an import file.
   

Specifying a stimulus order
~~~~~~~~~~~~~~~~~~~~~~~~~~~

A stimulus order is also specified on a single line. The general format of a line containing a stimulus order is ::

   order,<order-name>,<stim-name-a>,<stim-name-b>,<stim-name-c>,<stim-name-d>,...
   
The fields and their contents are:

*order*
   The word "order" indicates that this line contains a stimulus order.
   
*<order-name>*
   Replace this with the name for this order. The order name must be unique among the orders for this phase.
   
*<stim-name-x>*
   Replace this with the name(s) of the stimuli to be used in this order.
   
Below is an example of stimuli orders taken from the file *\"ross-sheehy.csv\"*: ::

   order,letters-plants-A,stim-letters-plants-1,stim-letters-plants-2,stim-letters-plants-3,stim-letters-plants-4,stim-letters-plants-5,stim-letters-plants-6
   order,letters-plants-B,stim-letters-plants-5,stim-letters-plants-6,stim-letters-plants-7,stim-letters-plants-8,stim-letters-plants-9,stim-letters-plants-10
   order,plants-letters-A,stim-plants-letters-1,stim-plants-letters-2,stim-plants-letters-3,stim-plants-letters-4,stim-plants-letters-5,stim-plants-letters-6

 
Additional examples
~~~~~~~~~~~~~~~~~~~
 
Additional examples are included with your habit installation (as of Habit 2.2.5). Each new workspace folder contains 
a link to a folder called "misc", which has several example files, some of which are shown :doc:`here<_import_examples>`.
 