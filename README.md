# Skipper and Skeeto timing
Various files and tools useful when timing Skipper and Skeeto speedruns.

## Icons
Icons in the `icons` folder can for instance be used for splits with [LiveSplit](https://livesplit.org). They are 
currently quadratic, but other than that there's no specific size criterion for now.

## AutoSplit
The images in the `auto-split` folder can be used with [AutoSplit](https://github.com/Toufool/Auto-Split) in order to 
automatically split when those images (within a threshold) are shown in the game. The images all have threshold and 
pause times properties in their filename as defined by the AutoSplit guides. This means those properties doesn't need to 
be set up in AutoSplit.

A prerequisite for AutoSplit is that the images are in alphabetical order of appeareance and they (except for dummy 
images) match 1:1 with the splits they represents. For some games, the order of splits are quite straigt forward as 
there's (roughly) only one route thorugh the game, but for other games there might be various routes based on personal
preferences. Each game section describes if there's anything special to be aware of.

### Games
#### Skipper and Skeeto 1
There's (for now?) not a "golden route" in this games, it's really up to personal preference. Therefore there is a bit
of work needed to be done before being able to work with AutoSplit:

1. Create a new folder where all your split images will be placed
2. Move/copy the images that matches splits you want (for 1st edition of this game, ignore the last split for now)
3. Order the images alphabetically by renaming them based on their appereances. This can for instance be done by 
prepending their filenames with `01_`, `02_`, `03_` etc. to their filename
4. Move/copy the image starting with `start_auto_splitter` - this doesn't need to be renamed
5. Specific for 1st edition:
   1. Find the image that matches the last scene in your route. Rename the image so it's ordered last, for instance if 
   the second last is prepended with `07_`, this one should be preprended with `08_` 
   2. Append `_{d}` to the title of the image (before `.png` if you can see the file extension). This makes it into a 
   dummy image (which makes sense in the next step)
   3. Move/copy the image starting with `finish` and rename it so it's ordered as the last image (right after the dummy 
   image). The dummy-image in the previous step does not trigger the last split, but rather makes sure we are in the
   final scene. When leaving that scene the screen gets black and the final image triggers the final split and stops 
   the time at the correct point as described by the rules

There are currently no strict rules for when the screenshot has been made and a split is triggered. For instance when 
scaring the cat it's triggered right when the dog is placed on the ground, but when the ludo dice is delivered to the 
fish it isn't triggered until the fish starts speaking. This is often due to there aren't any unique characteristics 
until then or the threshold isn't large enough - this is for instance also why the shed closet isn't triggered right 
away. Some of the events might be possible to optimize, but as long as they are consistent across runs it shouldn't be 
an issue.

Finally, the list of images are of course not complete, mostly because some events doesn't seem to have a clear trigger.
The biggest "issue" for now is that there's a big gap between start of the run and the first split, but that's due to 
it's much easier to trigger task splits (for instance scaring an enemy or helping a friend) compared to picking up an
item as the items are placed "randomly" in the inventory. 
