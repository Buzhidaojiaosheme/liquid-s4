# Results

## First rounds:
### Testing with the dataset HR and a epoch limit of 500

====================== Summary ======================
Mode              : Best f : Steps : Time            
----------------  : ----   : ----  : ----            
Initial solution  : 0.1248 : 1     : 10:50:04 (h:m:s)
Random seeding    : 0.1026 : 1     : 20:50:46 (h:m:s)
----------------  : ----   : ----  : ----            
Total             : 0.1026 : 2     : 20:50:46 (h:m:s)
=====================================================
0.10261257737874985: {'n_layers': 6, 'd_model': 177, 'prenorm': True, 'd_state': 239, 'lr': 0.001, 'bidirectional': True, 'optimizer_lr': 0.009}

### Epoch limit of 100

====================== Summary ======================
Mode              : Best f : Steps : Time            
----------------  : ----   : ----  : ----            
Initial solution  : 0.2334 : 1     : 02:08:49 (h:m:s)
Random seeding    : 178.9  : 1     : 06:05:15 (h:m:s)
----------------  : ----   : ----  : ----            
Total             : 0.2334 : 2     : 06:05:15 (h:m:s)
=====================================================
HR: 0.23336294293403625 {'n_layers': 5, 'd_model': 144, 'prenorm': True, 'd_state': 132, 'lr': 0.001, 'bidirectional': True, 'optimizer_lr': 0.007}

====================== Summary ======================
Mode              : Best f : Steps : Time            
----------------  : ----   : ----  : ----            
Initial solution  : 0.2334 : 1     : 02:16:53 (h:m:s)
Local sampling    : 0.2226 : 2     : 06:08:03 (h:m:s)
----------------  : ----   : ----  : ----            
Total             : 0.2226 : 3     : 08:24:55 (h:m:s)
=====================================================
HR: 0.22263099253177643 {'n_layers': 5, 'd_model': 176, 'prenorm': True, 'd_state': 182, 'lr': 0.001, 'bidirectional': True, 'optimizer_lr': 0.007}

^ Testing using 500 epochs results in 'final/test/mse': 0.11240249127149582

### RR
======================= Summary ======================
Mode              : Best f  : Steps : Time            
----------------  : ----    : ----  : ----            
Initial solution  : 0.1436  : 1     : 02:15:18 (h:m:s)
Local sampling    : 0.07713 : 2     : 04:03:07 (h:m:s)
----------------  : ----    : ----  : ----            
Total             : 0.07713 : 3     : 06:18:24 (h:m:s)
======================================================
RR: 0.07713264971971512 {'n_layers': 5, 'd_model': 200, 'prenorm': True, 'd_state': 160, 'lr': 0.0004, 'bidirectional': True, 'optimizer_lr': 0.008}

^ Testing using 500 epochs results in 'final/test/mse': 0.06275124847888947

### SpO2
======================= Summary ======================
Mode              : Best f  : Steps : Time            
----------------  : ----    : ----  : ----            
Initial solution  : 0.04958 : 1     : 02:18:03 (h:m:s)
Local sampling    : 0.01902 : 3     : 05:13:27 (h:m:s)
----------------  : ----    : ----  : ----            
Total             : 0.01902 : 4     : 07:31:29 (h:m:s)
======================================================
SpO2: 0.019023045897483826 {'n_layers': 5, 'd_model': 92, 'prenorm': False, 'd_state': 124, 'lr': 0.0004, 'bidirectional': True, 'optimizer_lr': 0.006}

^ Testing using 500 epochs reuslts in 'final/test/loss': 0.006862881127744913


Best HR, RR, SpO2 results: 
- outputs/2023-09-05/09-51-51-480607
- outputs/2023-09-04/10-09-50-848632
- outputs/2023-09-03/18-46-39-154549

