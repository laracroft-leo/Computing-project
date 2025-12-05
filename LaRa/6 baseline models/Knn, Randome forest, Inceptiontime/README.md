The *all folds* version automatically runs through all folds in one go. The other version requires manually entering the fold index each time.

For example, in the file **LaRa-knn,rf,inceptiontime fold 0-5.ipynb**, the currently running fold is fold 5. Before this, we had already manually run folds 0, 1, 2, 3, and 4. Each time, we entered the fold number, restarted the session, and then ran the notebook starting from step 5. At the end, the code aggregates and summarises the results from folds 0, 1, 2, 3, 4, and 5 together.

The number of folds is equal to the number of subjects. In the LARa dataset we used 8 subjects and applied Leave-One-Subject-Out (each time leaving 1 person out for testing), so there are 8 folds: in each fold, 1 subject is used as the test set and the remaining 7 subjects form the training set, and this is repeated 8 times in rotation.

The red-highlighted parts below:
/usr/local/lib/python3.12/dist-packages/sklearn/metrics/_classification.py:2524: UserWarning: y_pred contains classes not in y_true warnings.warn("y_pred contains classes not in y_true")
These are not code crashes, just warnings. They mean that for some subjects, the test set does not contain all 8 activity classes, so certain classes in some folds are not included in the per-fold metric computation.


