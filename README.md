# TrackMateAnalyzer
 Batch compile and analyze trackmate track results


### Directions
1. Create a folder for each condition of data (ex. wildtype cells vs mutant cells)
2. Run TrackMate on Fiji/ImageJ, on the Display Options page, select 'Tracks' at the bottom. In the pop up window 'Track tables', select 'Tracks', then export to CSV. Save the CSV into a subfolder within the appropriate condition folder (keep the name as the default 'export.csv'). 

    Example directory: C:\Users\username\Desktop\ExperimentReplicates\Replicate1\Condition1\TrackMateFolder1\export.csv\

    If you only have one replicate of the experiment: C:\Users\username\Desktop\TrackMateExperiment\Condition1\TrackMateFolder1\export.csv\

3. Run the following script, it will ask for several prompts:

    a. Enter the number of conditions to be analyzed (statistical analysis necessitates at least 2 conditions)

    b. Enter the name of each condition to be analyzed (ex. wildtype and mutant), it is essential these names match the name of the condition folder and if you are analyzing multiple replicates, the condition folders have the same names across different replicate folders

    c. Enter the minimum track duration (sec) you would like (this will filter out all tracks under the number you enter, so if you enter 10, all the data will be from tracks that had a duration of at least 10 seconds)

    d. Enter 'Y' if you would like to analyze more than one replicate (a replicate is a single iteration of an experiment, analyzing multiple replicates would mean you would like to combine the data across multiple iterations of an experiment), 'N' if you would like to analyze a single replicate

    e. Enter 'Y' if you would like to normalize the conditions to the mean of condition1 (this is the first condition name you enter, I recommend entering your control or wt condition first), the normalization occurs by: conditionX_value*(conditionX_mean/condition1_mean). Enter 'N' if you do not want to normalize the data.

    f. A window will pop up to ask for the directory to analyze. If you are analyzing multiple replicates, select the directory that contains the folders for each replicate of the experiment. If you are analyzing a single replicate, choose the folder of the single replicate.

        Multiple Replicates Example Directory: C:\Users\username\Desktop\ExperimentReplicates

        Single Replicate Example Directory: C:\Users\username\Desktop\ExperimentReplicates\Replicate1 
    

### Troubleshooting Tips
1. Confirm that all your trackmate files are called 'export.csv' and they are each located in an individual folder within each condition folder
2. Confirm you entering the correct condition names and that these match the name of the condition folders exactly, and these are the same condition names across multiple folders
3. If you are analyzing multiple replicates, make sure the only folders in your chosen directory are the replicate folders (aside from trackmate_results folder if have already run the script)


Developed by Oliver Sterling-Angus https://github.com/oes6098