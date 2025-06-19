# Mouse Behavioral Action Segmentation Research

This repository contains code developed for computational neuroscience research conducted at the Zuckerman Mind Brain and Behavior Institute at Columbia University. The research focused on quantifying mouse behavior during a standardized decision-making task using pose estimates and behavioral action segmentation. In the experimental setup, mice were required to turn a wheel to move a visual stimulus to the center of a screen to receive rewards. Our efforts were at tracking the spatial orientation of mouse body parts in order to predict discrete behavioral states the mouse was in as it performed the task.

![Diagnostics](https://github.com/user-attachments/assets/cd0dca2d-c497-4ed1-822c-69451a287111)
   
## Diagnostic Pipeline Development

My contributions in particular were aimed at developing diagnostic tools to assess the efficacy of the group Temporal Convolutional Network (TCN) model architectures for predicting behavioral states as well as identifying any unique behavioral fingerprints of the individual mice across the experimental sessions. 

I developed a comprehensive diagnostic pipeline to evaluate model performance which processed multiple time series data sources including:

- Wheel velocity measurements
- Mouse paw movement trajectories  
- Temporal event markers (first wheel movement, stimulus centering, etc.)

The pipeline overlays model predictions (four discrete states: **Still**, **Move**, **Wheel Turn**, **Groom**) with the time series data to validate prediction accuracy through event-aligned analysis.

## Behavioral Fingerprinting Analysis

Following model evaluation, I implemented methods to identify unique behavioral signatures across experimental sessions by:

- Developing vectorization approaches for mouse behavioral patterns
- Implementing clustering algorithms to group similar behavioral profiles
- Analyzing within-subject and cross-session consistency

## Technical Implementation

### Technology Stack

- **Python** - Primary programming language
- **NumPy** - Numerical computing and array operations
- **Matplotlib** - Data visualization and plotting
- **IBL (International Brain Lab) packages** - Specialized neuroscience data analysis tools

### Key System Components

#### 1. TCN Model Integration

- **Input**: Temporal sequences of body part positions and velocities
- **Output**: Probability distributions over 4 behavioral states
- **Post-processing**: State prediction clipping and temporal alignment across data sources

#### 2. Data Quality & Preprocessing Pipeline

- **Likelihood thresholding**: Filtering low-confidence tracking data to improve model input quality
- **Temporal smoothing**: Balancing noise reduction while preserving temporal dynamics
- **Body part standardization**: Focus on right paw tracking for consistent movement analysis

#### 3. Advanced Visualization System

- **Predicted state heatmaps**: Temporal visualization of behavioral state predictions
- **State frequency analysis**: Statistical distribution analysis across behavioral states
- **State duration analysis**: Temporal dynamics of behavioral state transitions
- **Video overlay system**: Real-time state prediction visualization on behavioral recordings

#### 4. Event-Aligned Analysis

- **Peri-event analysis**: Quantifying behavioral state changes around specific task events
- **Trial structure mapping**: Aligning behavioral states with distinct task phases
- **Feedback-based analysis**: Comparing behavioral patterns between correct/incorrect trials

#### 5. Cross-Session Behavioral Analysis

- **Within-subject consistency**: Measuring stability of individual behavioral patterns
- **Cross-session reliability**: Assessing behavioral state consistency across experimental days  
- **Individual difference identification**: Detecting unique behavioral signatures per mouse


---

*This research was conducted at the Zuckerman Mind Brain and Behavior Institute, Columbia University, as part of ongoing efforts to understand the computational principles underlying decision-making behavior in animal models.*
