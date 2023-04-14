# granular_test
 
UPDATE: fix achieved, thanks to Donnerbono and giuliomoro on the bela forums. Link here: https://forum.bela.io/d/3017-cpu-issues-can-not-get-my-patch-to-run-well/4

Essentially the culprit appears to have been the bob~ object, unsurprisingly. This was in a section of the patch designed for sampling, which I wasn't even using. I've removed it (and a few other GUI things) and it works much better. I've updated the patch with 3 instances of the granular patch running at once, which seems to work well.

--

This is a test patch to try and figure out why my Pure Data granular patch runs so poorly on a Bela board. 

It's a granular patch with one sound file and 4 grain voices, triggered quite slowly. This seems to run extremely poorly and usually crashes at any buffer size on a Bela.
