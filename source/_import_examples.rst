Stimulus and Stimulus Order import examples
===========================================

Below are some examples of files that can be used to import stimuli to a phase of a Habit experiment. These files are 
included with habit (as of version 2.2.5), and are in the *misc* folder of new workspaces created with this version. 

Ross-Sheehy
-----------

This experiment has a single phase. The example below imports dual stimuli and several orders that phase. All of the 
stimuli files are specified with a relative path (does not begin with a drive letter or \"/\"), so the path given will
be appended to the *Stimulus Root Folder*. ::

   stim,stim-letters-plants-1,left,examples/images/letters/A.jpg,right,examples/images/plants/alumroot.jpg,,
   stim,stim-letters-plants-2,left,examples/images/letters/B.jpg,right,examples/images/plants/butterflyweed.jpg,,
   stim,stim-letters-plants-3,left,examples/images/letters/C.jpg,right,examples/images/plants/chamomile.jpg,,
   stim,stim-letters-plants-4,left,examples/images/letters/D.jpg,right,examples/images/plants/dogwood.jpg,,
   stim,stim-letters-plants-5,left,examples/images/letters/E.jpg,right,examples/images/plants/ginger.jpg,,
   stim,stim-letters-plants-6,left,examples/images/letters/F.jpg,right,examples/images/plants/ginseng.jpg,,
   stim,stim-letters-plants-7,left,examples/images/letters/G.jpg,right,examples/images/plants/indigo.jpg,,
   stim,stim-letters-plants-8,left,examples/images/letters/H.jpg,right,examples/images/plants/pennyroyal.jpg,,
   stim,stim-letters-plants-9,left,examples/images/letters/J.jpg,right,examples/images/plants/spicewood.jpg,,
   stim,stim-letters-plants-10,left,examples/images/letters/K.jpg,right,examples/images/plants/yellowwort.jpg,,
   stim,stim-plants-letters-1,left,examples/images/plants/alumroot.jpg,right,examples/images/letters/A.jpg,,
   stim,stim-plants-letters-2,left,examples/images/plants/butterflyweed.jpg,right,examples/images/letters/B.jpg,,
   stim,stim-plants-letters-3,left,examples/images/plants/chamomile.jpg,right,examples/images/letters/C.jpg,,
   stim,stim-plants-letters-4,left,examples/images/plants/dogwood.jpg,right,examples/images/letters/D.jpg,,
   stim,stim-plants-letters-5,left,examples/images/plants/ginger.jpg,right,examples/images/letters/E.jpg,,
   stim,stim-plants-letters-6,left,examples/images/plants/ginseng.jpg,right,examples/images/letters/F.jpg,,
   stim,stim-plants-letters-7,left,examples/images/plants/indigo.jpg,right,examples/images/letters/G.jpg,,
   stim,stim-plants-letters-8,left,examples/images/plants/pennyroyal.jpg,right,examples/images/letters/H.jpg,,
   stim,stim-plants-letters-9,left,examples/images/plants/spicewood.jpg,right,examples/images/letters/J.jpg,,
   stim,stim-plants-letters-10,left,examples/images/plants/yellowwort.jpg,right,examples/images/letters/K.jpg,,
   order,letters-plants-A,stim-letters-plants-1,stim-letters-plants-2,stim-letters-plants-3,stim-letters-plants-4,stim-letters-plants-5,stim-letters-plants-6
   order,letters-plants-B,stim-letters-plants-5,stim-letters-plants-6,stim-letters-plants-7,stim-letters-plants-8,stim-letters-plants-9,stim-letters-plants-10
   order,plants-letters-A,stim-plants-letters-1,stim-plants-letters-2,stim-plants-letters-3,stim-plants-letters-4,stim-plants-letters-5,stim-plants-letters-6
   order,plants-letters-B,stim-plants-letters-5,stim-plants-letters-6,stim-plants-letters-7,stim-plants-letters-8,stim-plants-letters-9,stim-plants-letters-10  


Baumgartner
-----------

This experiment has two phases, "Habituation" and "Test", and uses a single stimulus. 
Below is the import for the *Habituation* phase. ::

   stim,h1,center,examples/images/animals/fox.jpeg,,,,,,,,,,,,,,
   stim,h2,center,examples/images/animals/hedgehog.jpeg,,,,,,,,,,,,,,
   stim,h3,center,examples/images/animals/zebra.jpeg,,,,,,,,,,,,,,
   stim,h4,center,examples/images/animals/seals.jpeg,,,,,,,,,,,,,,
   stim,h5,center,examples/images/animals/frog.jpeg,,,,,,,,,,,,,,
   stim,h6,center,examples/images/animals/hummingbird.jpeg,,,,,,,,,,,,,,
   stim,h7,center,examples/images/animals/tiger.jpeg,,,,,,,,,,,,,,
   stim,h8,center,examples/images/animals/lion.jpeg,,,,,,,,,,,,,,
   stim,h9,center,examples/images/animals/duck.jpeg,,,,,,,,,,,,,,
   stim,h10,center,examples/images/animals/chicken.jpeg,,,,,,,,,,,,,,
   stim,h11,center,examples/images/animals/goose.jpeg,,,,,,,,,,,,,,
   stim,h12,center,examples/images/animals/penguins.jpeg,,,,,,,,,,,,,,
   stim,h13,center,examples/images/animals/butterfly.jpeg,,,,,,,,,,,,,,
   stim,h14,center,examples/images/animals/bear.jpeg,,,,,,,,,,,,,,
   stim,h15,center,examples/images/animals/rabbits.jpg,,,,,,,,,,,,,,
   stim,h16,center,examples/images/animals/eagle.jpeg,,,,,,,,,,,,,,
   stim,h17,center,examples/images/animals/baboons.jpeg,,,,,,,,,,,,,,
   stim,h18,center,examples/images/animals/meerkat.jpeg,,,,,,,,,,,,,,
   order,orderA,h1,h2,h3,h4,h5,h6,h7,h8,h9,h10,h11,h12,h13,h14,h15,h16
   order,orderB,h2,h3,h4,h5,h6,h7,h8,h9,h10,h11,h12,h13,h14,h15,h16,h17
   order,orderC,h3,h4,h5,h6,h7,h8,h9,h10,h11,h12,h13,h14,h15,h16,h17,h18
   
The extra commas on the lines which specify stimuli are due to exporting this file from an excel spreadsheet. When selecting
a block of cells to export, one must select empty blocks at the end of the *stim* lines because the *order* lines use many
more cells. Habit will ignore these empty fields. 

Below is the import file for the *Test* phase. ::

   stim,t1,center,examples/images/fish/carp.jpg,,
   stim,t2,center,examples/images/fish/pike.jpg,,
   stim,t3,center,examples/images/fish/scad.jpg,,
   stim,t4,center,examples/images/fish/mackarel.jpg,,
   stim,t5,center,examples/images/fish/anchovy.jpg,,
   stim,t6,center,examples/images/fish/cod.jpg,,
   stim,t7,center,examples/images/fish/redeye.jpg,,
   stim,t8,center,examples/images/fish/blenny.jpg,,
   stim,t9,center,examples/images/fish/gurnard.jpg,,
   stim,t10,center,examples/images/fish/angelshark.jpg,,
   stim,t11,center,examples/images/fish/chub.jpg,,
   stim,t12,center,examples/images/fish/dab.jpg,,
   order,testA,t1,t2,t3,t4
   order,testB,t5,t6,t7,t8
   order,testC,t9,t10,t11,t12
   
Additional examples can be found in the *misc* folder of a new workspace (must have been created with habit 2.2.5 or greater).    
