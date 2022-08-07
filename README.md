# GameDisk2

## How to update the Gamedisk2 from the Gamedisk repository and generate plz-files
1) Checkout the "Gamedisk2/master" branch
2) Fetch and merge the branch "Gamedisk/master" to the "Gamedisk2/master" to get the latest additions
   - Note: you might need to call "git fetch -all" to get all data from all remotes to the local repository
3) For any new games with data files, make the "*_data" folder in the same level the pop file is (e.g. "Action0/1nvader_data"), and copy the relevant data files there in the correct forder structure (e.g. "Action0/1nvader_data/music/1Invad_00.raw").
4) Run the python script (python 2.7) that generates the plz-file. The plz-file is a package file that contains the pop file and the data files compressed, with the correct folder structure.
```
   cd ServerTools
   python2 CreateIndices.py
```   
5) Add and update changes to the "Gamedisk2" repository 
```
   cd ..
   git add .
   git commit -m"generated plz-files"
   git push 
```
