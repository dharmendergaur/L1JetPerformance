# Level-1 Objects Performance Analyzer
Macros to analyze flat ntuples such as NANOAOD ntuples, L1 ntuples or private ntuples. 
## Quick Start
- Clone the repo:
  ```
  git@github.com:dharmendergaur/L1JetPerformance.git
  ```
- Merge the nano files together into one nano file (with:`hadd nano.root nano*.root`).
- Use as input for `performance_nano.py`in directory `L1JetPerformance/l1macros` (choose your preferred channel):
     ```
     python3 performances_nano.py -i _path_to_nano.root -o all_MuonJet.root -c MuonJet --reemul
     ```
  
- Make a directory called `plotsL1Run3` and make sure the root file is called `all_MuonJet.root` (or all_"channelName").
- Plot using the plotter in `L1JetPerformance/plotting` directory (choose your preferred channel and corresponding config card):
    ```
    python3 make_MuonJet_plots.py --dir ../l1macros --config ../config_cards/full_MuonJet.yaml
    ```

**Note:** For NanoAODv15 dataset, use the `NanoAODv15` branch. Clone with:
```
git@github.com:dharmendergaur/L1JetPerformance.git -b NanoAODv15
```

Go to specific subdirectories for more information.
