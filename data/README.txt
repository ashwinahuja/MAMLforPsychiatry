Dr Sarah Morgan, 11/02/2021

This folder contains the preliminary dataset for the coursework for R250: Applications of ML to Psychiatry.

COBRE_demographics.csv includes a list of subject ids, labels, sex and age information.
Labels: -1 for a healthy control subject, 1 for a patient with schizophrenia
Sex: -1 for male, 1 for female
PANSS total: these are symptom scores (from the Positive and Negative Syndrome Scale). Note controls do not have symptom data. Symptoms are also missing for 2 patients.

COBRE_cortical_thickness.csv includes cortical thickness measurements for all subjects, for 308 cortical brain regions.

COBRE_fmri_connectivity.mat is a Matlab file with connectivity data for all subjects. Subjects are listed in the same order as the demographics file above.
Note that not only 293 out of 308 brain regions have fmri data available (due to incomplete fMRI coverage of the brain- some regions have signal drop out). These 293 regions are listed in the file COBRE_fmri_regions.csv.
Also note that the values from the connectivity matrices are provided in vector format. To transform back to a connectivity matrix, you need to reshape the vectors.
E.g. in Matlab, use the command: matrix = reshape(connectivity_data(ind,:),[293,293])
where ind is an integer between 1 and 148 denoting the subject you are interested in. To check you have reshaped the matrix correctly, try plotting it- it should be a symmetric matrix with 1s on the diagonal.

COBRE_fmri_connectivity.csv- as above but saved as a .csv file.

COBRE_fmri_regions.csv- list of regions with fMRI data available (see above).
