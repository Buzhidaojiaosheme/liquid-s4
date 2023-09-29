Paper's Hyperparameters

HR Model testing (p=3):

========================== Summary =========================
Mode              : Best f : Steps : Time                   
----------------  : ----   : ----  : ----                   
Initial solution  : 0.1    : 1     : 1 day 15:56:10 (h:m:s) 
Local sampling    : 0.1079 : 1     : 20:30:27 (h:m:s)       
----------------  : ----   : ----  : ----                   
Total             : 0.1    : 2     : 2 days 12:26:38 (h:m:s)
============================================================
HR: 0.10000631958246231 {'n_layers': 6, 'd_model': 128, 'prenorm': [True, False], 'd_state': 256, 'lr': 0.001, 'bidirectional': [True, False], 'optimizer_lr': 0.005}

RMSE: 0.31623775799

RR Model testing (p=2):

========================== Summary ==========================
Mode              : Best f  : Steps : Time                   
----------------  : ----    : ----  : ----                   
Initial solution  : 0.03837 : 1     : 23:46:46 (h:m:s)       
Local sampling    : 0.06561 : 2     : 2 days 04:39:56 (h:m:s)
----------------  : ----    : ----  : ----                   
Total             : 0.03837 : 3     : 3 days 04:26:41 (h:m:s)
=============================================================
RR: 0.03836996108293533 {'n_layers': 6, 'd_model': 128, 'prenorm': [True, False], 'd_state': 256, 'lr': 0.001, 'bidirectional': [True, False], 'optimizer_lr': 0.01}

RMSE: 0.19588251857

SPO2 Model testing (p=4):

=========================== Summary ==========================
Mode              : Best f   : Steps : Time                   
----------------  : ----     : ----  : ----                   
Initial solution  : 0.005581 : 1     : 2 days 07:06:50 (h:m:s)
----------------  : ----     : ----  : ----                   
Total             : 0.005581 : 1     : 2 days 07:06:50 (h:m:s)
==============================================================
SpO2: 0.0055809663608670235 {'n_layers': 6, 'd_model': 128, 'prenorm': [True, False], 'd_state': 256, 'lr': 0.001, 'bidirectional': [True, False], 'optimizer_lr': 0.01}

RMSE: 0.07470586563

Output Files:
HR: outputs/2023-09-21/23-42-19-577102
RR: outputs/2023-09-20/08-41-13-434207
SpO2: outputs/2023-09-18/22-19-25-814014