# We recommend to isntall python with Anaconda3
# Before tyou run on Linux OS execute

pip install requirements.txt --use-feature=2020-resolver


# The main script of the code is CNN_Classification. It returns the training and testing confusion matrices as well as the
# training and testing accuracy performance for # each cell separately.

# The code is formulated to give performance results for the cases of the:
    # 3-class problem (AAC-BC, BISTR-SOM, CCK)
    # the 4-class problem (AAC-BC, BISTR-SOM, CCK, NPY)
    # the 5-class problem (AAC, BC, BISTR, CCK, SOM), and
    # the 6-class problem (AAC, BC, BISTR, SOM, CCK, NPY)
# depending on what the user will define.

# The following parameters are defined by the user:
#     num_iters: Number of iterations for the random train-test splits
#     epochs: Number of epochs required for the CNN model to be trained
#     loss_func: Loss function for the optimizer
#     learning_rate: Learning rate parameter for the optimizer
#     features: Number of features to feed the CNN model. The options for this parameter are the following
#         1: 1D-CNN is fed with calcium signal laps
#         2: 2D-CNN is fed with calcium-velocity signal laps
#         3: 2D-CNN is fed with calcium-velocity-zdepth signal laps
#     indexing: With this parameter the user defines the cell-types (either merged categories or separate cells)
#               that will be used in the classification procedure 
#     balance: This parameter defines the number of the training examples for the merged categories. The options for this parameter are the following
#         balanced: Same number of training examples for each category
#         stratified: It preserves the proportion of target as in original dataset, in the train datasets.
#     category: The options for this parameter are the following
#         min_categ: As a number of training examples for each category we use the number of examples from the category with the minimum number of examples. 
#         imbalanced: For each category we use all its available examples for training
#         semi_balanced: All categories start with the minimum number of training examples (min_categ)
                        and the user adds extra examples via the parameter size_increased, so that for each
                        category almost the same number of training examples are used.

#    size_increased: If category parameter is defined as semi_balanced, in size_increased the user defines how many examples should be added to each category. 
#    test_size: User defines the number of testing examples to be used from each category
#    step_laps: Number of laps to be merged
#    interp_timesteps: Length of the interpolated signal laps

#   authors: eirinitroul [AT] gmail [DOT] com; chavlis [DOT] spiros [AT] gmail [DOT] com