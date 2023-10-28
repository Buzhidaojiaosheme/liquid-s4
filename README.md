# Hyperparameter Tuning: Liquid State Space Models(S4) with PyHopper

## References & Dependencies

This repository is derived from the Liquid S4 state-space models repository, [raminmh/liquid-s4](https://github.com/raminmh/liquid-s4), which is based on preprint paper [https://arxiv.org/abs/2209.12951](https://arxiv.org/abs/2209.12951). 

Additionally, for hyperparameter fine tuning, the file train_pyhopper.py uses the library PyHopper found here: [https://github.com/pyhopper/pyhopper](https://github.com/pyhopper/pyhopper).

## Training using PyHopper

The file train_pyhopper.py is a modified version of train.py. There is an additional function called objective, which performs the following process: it takes in a config object, makes a copy of the OmegaConf object with the original config values found in bidmc/s4-bidmc, and updates the copy with the config object’s values. Instead of calling the train function directly in the main function, a PyHopper search object is created, with the testing ranges for each hyperparameter. The search object runs on the objective function. After the testing finishes, PyHopper’s results and search state are saved into *_search_results.txt and *_search_save.out, respectively.

The train_pyhopper.py can be run the same as how train.py is run in the liquid-s4 repository. The config file’s value for dataset.target needs to be set to the appropriate dataset when running the file.

## Round One of testing

The detailed results and outputs of round one of testing can be found in round1_testing.

Heart Rate
- Best loss: 0.22263099253177643 (MSE)
- Best params: {'n_layers': 5, 'd_model': 176, 'prenorm': True, 'd_state': 182, 'lr': 0.001, 'bidirectional': True, 'optimizer_lr': 0.007}

Respiratory rate
- Best loss: 0.07713264971971512 (MSE)
- Best params: {'n_layers': 5, 'd_model': 200, 'prenorm': True, 'd_state': 160, 'lr': 0.0004, 'bidirectional': True, 'optimizer_lr': 0.008}
SpO2
- Best loss: 0.019023045897483826 (MSE)
- Best params: {'n_layers': 5, 'd_model': 92, 'prenorm': False, 'd_state': 124, 'lr': 0.0004, 'bidirectional': True, 'optimizer_lr': 0.006}

## Round Two of testing

The detailed results and outputs of round one of testing can be found in round2_testing.

Instead of randomized starting values for the PyHopper search, the initial values are set to values stated in the “Liquid Structural State-Space Models” paper.

Heart Rate
- Best loss: 0.10000631958246231(MSE)

Respiratory Rate
- Best loss: 0.03836996108293533 (MSE)

SpO2
- Best loss: 0.0055809663608670235(MSE)

PyHopper found that the “Liquid Structural State-Space Models” paper’s hyperparameters are optimal.
