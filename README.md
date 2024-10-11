# Mimicking Human Attention in Driving Scenarios for Enhanced Visual Question Answering: Insights from Eye-Tracking and the Human Attention Filter

Welcome to the repository for the research paper **"Mimicking Human Attention in Driving Scenarios for Enhanced Visual Question Answering: Insights from Eye-Tracking and the Human Attention Filter"**. This repository contains the **DriVQA dataset** along with other key elements, including eye-tracking data and attention maps, all used to study human attention in driving scenarios and its application in improving Visual Question Answering (VQA) systems.

## DriVQA Dataset Overview

The **DriVQA dataset** includes data gathered from an experiment conducted with **34 participants**. Each participant was presented with **24 driving scenarios** and asked two questions related to each scenario. The experiment captures both the participants' answers and their eye movements using Tobii Studio's eye-tracking software. The dataset is organized as follows:

### 1. **Driving Scenarios (Images)**
   - A total of **24 driving scenario images**.
   - Each image depicts a unique driving situation where attention and decision-making are critical.

### 2. **Participant Responses**
   - The folder `Responses` contains a `.xlsx` file that records participants' answers.
   - Each participant has a dedicated sheet named according to their anonymized ID (e.g., P01, P02, etc.).
   - A total of **1632 answers** have been recorded, with each participant answering two questions per scenario.

### 3. **Eye-Tracking Data**
   The eye-tracking data has been processed into two formats to study visual attention:
   
   - **Gaze Plots**: 
     - Found in the folder `Gaze Plot`, each gaze plot represents the sequence of focus points on the image. The size of the points corresponds to the duration of attention.
     - There are **1632 gaze plots** in total (2 per scenario per participant).
   
   - **Heatmaps**: 
     - Located in the folder `Heatmap`, these heatmaps visualize the concentration of gaze points and their duration in specific scene areas.
     - The heatmaps are generated using Tobii Studio 3.4.5 and illustrate the areas of the image that received the most attention.
     - There are **1632 heatmaps** in total (2 per scenario per participant).

### 4. **Attention Maps**
   - Attention maps are created by applying a Gaussian blur to the gaze points and mapping them onto a grid over the scene image.
   - These maps simulate the distribution of visual attention.
   - The maps are available in the respective participant folders within the `Gaze Plot` and `Heatmap` directories.

### 5. **Case Studies**
   - A separate folder `Case Studies` contains heatmaps generated from a case study that applied the attention data to state-of-the-art Visual Question Answering (VQA) models, **LXMERT** and **ViLBERT**. 
   - The results provide insights into how these models perform compared to human attention.

## Dataset Structure

```
├── DriVQA
│   ├── Test 1
│   │   ├── P01
│   │   │   ├── Gaze Plot
│   │   │   ├── Heatmap
│   │   └── ...
│   ├── Test 2
│   │   ├── P01
│   │   │   ├── Gaze Plot
│   │   │   ├── Heatmap
│   │   └── ...
├── Responses
│   └── responses.xlsx
├── Case Studies
│   ├── LXMERT
│   ├── ViLBERT
└── README.md
```

## Key Elements
- **24 driving images** representing various driving scenarios.
- **48 questions** associated with the scenarios (two questions per scenario).
- **1632 answers** collected from participants.
- **1632 gaze plots** showing participants' focus sequences.
- **1632 heatmaps** illustrating attention intensity across the scenarios.

## How to Use the Dataset

1. **Visualize Attention**: 
   Use the gaze plots and heatmaps to understand how participants visually process different driving scenarios.

2. **Analyze Responses**: 
   Access participant answers in the `responses.xlsx` file to see how human attention correlates with decision-making in driving scenarios.

3. **Case Studies on VQA Models**: 
   Explore the case study data in the `Case Studies` folder to compare human attention with VQA models such as LXMERT and ViLBERT.

## License and Citation
If you use the DriVQA dataset in your research, please cite the following paper:

```
@article{author2024mimicking,
  title={Mimicking Human Attention in Driving Scenarios for Enhanced Visual Question Answering: Insights from Eye-Tracking and the Human Attention Filter},
  author={Kaavya Rekanar et al.},
  journal={...},
  year={2025}
}
```

## Acknowledgments
We would like to thank all the participants in the study, as well as the development team of Tobii Studio 3.4.5 for their eye-tracking software that was instrumental in creating the attention maps.

---

For further questions or clarifications, feel free to reach out via the repository's issues page.
