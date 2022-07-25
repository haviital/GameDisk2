# GameDisk2

## How to update the Gamedisk2 from the Gamedisk repository and generate plz-files
1) Checkout the "Gamedisk2/master" branch
2) Fetch and merge the repository "Gamedisk/master" to the "Gamedisk2/master" to get the latest additions
3) For any new games with data files, make the "*_data" folder in the same level the pop file is (e.g. "Arcade0/1nvader_data"), and copy the relevant data files there in the correct forder structure (e.g. "Arcade/1nvader_data/music/1Invad_00.raw").
4) Run the python script (python 2.7) that generates the plz-file. The plz-file is a package file that contains the pop file and the data files compressed, with the correct folder structure.
   - "cd ServerTools"
   - "python2 CreateIndices.py"
5) "cd .."
6) "git add ."
7) "git commit -m"generate plz-files"
8) "git push" 
