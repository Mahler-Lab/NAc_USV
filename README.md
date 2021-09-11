# NAc_USV
All code generated with the project Nucleus Accumbens Chemogenetic Inhibition Suppresses Amphetamine-Induced Ultrasonic Vocalizations in Male and Female Rats

## Abstract
Adult rats emit ultrasonic vocalizations (USVs) related to their affective states, potentially providing information about their subjective experiences during behavioral
neuroscience experiments. If so, USVs might provide an important link between invasive animal preclinical studies and human studies in which subjective states can be readily
queried. Here, we induced USVs in male and female Long Evans rats using acute amphetamine (2 mg/kg), and asked how reversibly inhibiting nucleus accumbens neurons using designer
receptors exclusively activated by designer drugs (DREADDs) impacts USV production. We analyzed USV characteristics using “Deepsqueak” software, and manually categorized detected
calls into four previously-defined subtypes. We found that systemic administration of the DREADD agonist clozapine-n-oxide, rel-ative to vehicle in the same rats, suppressed the
number of frequency modulated and trill-containing USVs without impacting high frequency, unmodulated (flat) USVs, nor the small number of low frequency USVs observed. Using 
chemogenetics, these results thus confirm that nucleus accumbens neurons are essential for production of amphetamine-induced frequency modulated USVs. They also support the 
promise of further investigating the characteristics and subcategories of these calls as a window into the subjective effects of neural manipulations with potential future 
clinical applications.

## USV detection and Labeling
DeepSqueak software (DeepSqueak 2.0 with MATLAB, https://github.com/DrCoffey/DeepSqueak) was employed to detect USVs and identify the detailed characteristics of human-verified USVs from this dataset. Audio files were
run though DeepSqueak’s All Short Call neural network, then a post-hoc denoiser trained on noise inherent to the experimental setup automatically excluded non-USVs from the 
dataset. Call statistics for accepted USVs (20-100 kHz) were calculated using the spectrotemporal contours output by the detection network. These statistics included each call’s 
1) principal frequency (average frequency over the call), 
2) change in frequency over the course of the call, 
3) sinuosity (length of the path between the first and last points on the contour, divided by the Euclidean distance between the first and last points), and 
4) duration.  

USVs identified by Deepsqueak were verified by a trained observer who was blind to experimental conditions. The observer verified around 95% of DeepSqueak-identified calls as
valid, with 4,160 calls out of 77,454 rejected as noise. USVs were visualized in spectrograms, which allowed inspection of call frequency over time. Putative calls were greater
than 2 ms and were confirmed by the observer listening to them on headphones (frequency was transduced into the audible range by playing calls at 0.05 speed for this confirmatory
evaluation). Identified calls were manually categorized into 1 of 4 categories: 1) Low Frequency (LF) calls, which were between 20-30 kHz, 2) Flat high frequency calls, which were 
between 30-100 kHz in principal frequency, and which lacked visible frequency modulation, 3) Frequency Modulated (FM) calls, which had visible frequency modulation without a trill
component, and 4) Trills, which had the same definitional criteria as FMs, but which also contained at least 8 ms and 2 cycles of rapid oscillating frequency.
