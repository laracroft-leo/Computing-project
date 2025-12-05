In the **DeepConvContext – LSTM variant – 1-layer – bidirectional.ipynb** file, the large red sections are not code errors; they are output from model performance tuning.

For example, one of the sections means:
The first time this matrix operation is run, the system automatically tries more than twenty different GPU algorithms “behind the scenes”. It spends some time compiling them and measuring which one is the fastest, then remembers the best one. The next time it encounters the same operation, it directly uses that fastest version, so the code runs more quickly.
