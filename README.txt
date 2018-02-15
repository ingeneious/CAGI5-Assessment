########### Scripts for CAGI challenges assessment ##################

## REQUIREMENTS ##

R:
>install.packages('ROCR')
>install.packages('plotrix')

## USAGE ##

to run all analyses, you have just to run the following script (Rscript CAGI_assessment_main_V03_FR.R)
CAGI_assessment_main_V03_FR.R: 
      This is the script that checks submission format, computes all statistics and makes plots
      This script expects a folder structure like this to run:
      ./src <- contains all scripts
      ./results <- will contain all performance tables and plots
      ./data <- has to contain 3 folders: experimental_value, submissions, template 
      
      These are Input needed:
            # experimental values file  in ./data/experimental_value
            # submission template in ./data/template
            # submission files in ./data/submissions

      Running the script these Output files will be generated in ./results
           # scatterplot of Experimental vs Predicted data NOTE: axis size are based on the min and max value of predicted values  
           # scatterplot of Experimental vs Predicted data NOTE: axis size are based on the min and max value of experimental data. Predicted values outside experimental range are replaced by the min or max value of experimental data (red dots in the scatterplot).
           # table containing all preformance indices (	RMSE, PCC, KCC, Sens, Spec, Bal. Acc, AUC). NOTE: script is able to manage more or no threshold for calculating AUC
           # table containing prediction rank for KCC, RMSE, AUC
           # heatmap of PCC  between submissions indices (only KCC, RMSE, AUC are taken in account)
