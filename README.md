# Knesset_24_Regression
Regression project - finding &amp; predicting the number of rows likud's speakers (all together) speak in each session in knesset 24. Competition based project, features are unknown and need to be handeled before regression.

Best practice according to all model trained (including checking Random Forest Regressor and Count Vectorizer feature/ TF-IDF) is using 2 features: note_count and party_size. note_count counts the notes in each text and party_size was scraped from the knesset website and wikipedia as well.

For best practice refer to notebook "Linear_Party_Size_Note_Count.ipynb" and the relevant pkl in the pkl folder.

Things you might want to know:
Stratified K Fold was used because of great imbalance in number of likud rows between each session.
Used Standard Scaler for scaling features.
Strong linear connection was shown through work progress (refer to Regression_Knesset_Project.ipynb) between note_count and likud party. (tried using log_note_count but no improvement was seen).

In all notebook models you need to activate Block 1 that trains the model with the processed_combined_data.csv (it is in the files for block 1 folder) which was made after imputing and a little cleaning of the very dirty dataset we recieved in the competition. All pkl files were saved and you can find them in the pkl folder or generate them using the processed data + block 1.

In block 2 you have a run_model function, which you can run with session_127.csv and session_127 with no likud rows csv (both csv's are in the files for block 2 folder) or run your own unseen data (for R2 you need to run more than one session otherwise you get nan).

All results are summed up nicely in tables inside the notebooks.

Points for improvement: hyper parameters in TF-IDF and using pca clustering. For future reference.

Note: Original notebook "Regression_Knesset_Project.ipynb" contains the combined work of the data scientists contributing for this competition:
Ortal Lasry , email: ortalgr@gmail.com
Or Raviv Cohen, email: or.cohen.raviv@gmail.com

