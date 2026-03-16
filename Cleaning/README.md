
# Data processing

## Run BlendICu ???

Not sure but I guess

## Notebook cleaning

Notebooks must be run in order to process the data. What each notebook does is detailed below.

### 1_add_baseline_covariates

Add baseline variables from flat, labels (all found in labels) to ltm.parquet. This is a bit time consuming. So, once done and stored as ltm.parquet, need not come back to this.

### 2_subsample

Rename and subsample to 2000

### 3_grids_data

Create grid of 12h and add mean and last known.

### 4_clean_time_varying_covariates

Not sure but I guess

### 5_clean_discharge_n_outcome

1. Remove admission_ids which have both icu_mortality and mortality_after_discharge as True
2. Remove row in each admission which are very close (<=5 hrs) to discharge. This is to avoid data 
3. leakage on discharge decision.
4. Add A
5. Add Y (Mortality within 7 days after discharge)
6. Add D (In-ICU mortality as a competing event)






