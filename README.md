# Adam Prime
Hi! This is our final project for EECS 227B: Convex Optimization. We benchmark the performance of different variants of the Adam optimizer. This was written by Kush Hari, Satvik Sharma, and Simeon Adebola. This repo was built from the DeepOBS suite: https://github.com/fsschneider/DeepOBS.

## Installation
```
cd ~/AdamPrime
conda env create -f environment.yaml
conda activate adam_prime
```

## Run Performance Experiment (NOTE: This could take several hours or even days depending on compute)
```
cd ~/AdamPrime/src/deepobs/
bash performance_experiments.bash
```

## Run Performance Analysis
```
cd ~/AdamPrime/src/deepobs/
mv results performance_results
python performance_analysis.py
```

## Run Beta Ablation Experiment
```
cd ~/AdamPrime/src/deepobs/
bash beta_ablation_quadratic_deep.bash
```

## Run Beta Ablation Analysis
I wasn't able to automate this last part of the code, but within the results folder, for each optimizer you should see 16 folders representing each run. Categorize them into groups of 4 based on the beta1 value and make separate folders. Then, add the beta_analysis script to each of those folders and run it. You can see a sample of it in the beta_results folder.
