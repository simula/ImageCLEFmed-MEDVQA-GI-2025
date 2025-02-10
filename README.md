# ImageCLEFmed-MEDVQA-GI-2025

The **ImageCLEFmed-MEDVQA-GI (3rd edition)** challenge focuses on integrating Visual Question Answering (VQA) with synthetic gastrointestinal (GI) data to enhance diagnostic accuracy and AI learning algorithms. This year's challenge includes two subtasks designed to push the boundaries of both image analysis and synthetic medical image generation, aiming to improve diagnostic processes and patient outcomes.

## Task Descriptions

### Subtask 1: Algorithm Development for Question Interpretation and Response

This task challenges participants to develop algorithms capable of accurately interpreting and responding to questions based on GI images. These questions may range from identifying abnormalities to describing image content. The focus is on creating robust systems that aid medical diagnostics by combining image and text understanding.

#### Example Questions:

-   How many polyps are in the image?
-   Are there any abnormalities in the image?
-   What disease is visible in the image?

### Subtask 2: Creation of High-Fidelity Synthetic GI Images

Participants in this subtask are tasked with generating synthetic GI images that closely resemble real medical images in detail and variability. These images should be realistic enough to support diagnostic systems effectively, providing a privacy-preserving alternative to real patient data.

## Data

The dataset for 2025 is an extended version of the HyperKvasir dataset ([datasets.simula.no/hyper-kvasir](https://datasets.simula.no/hyper-kvasir)) and includes:

-   GI images with detailed Visual Question Answering (VQA) annotations.
-   New synthetic image data created to simulate realistic diagnostic scenarios.
-   Segmentation masks for key image elements like polyps and instruments.

*   **Development Dataset \[ Coming Soon \]**
*   **Test Dataset \[ Coming Soon \]**

## Evaluation Methodology

### Subtask 1: Question Interpretation and Response

-   **Metrics**: Accuracy, Precision, Recall, F1 Score.
-   Submissions will be evaluated on the correctness and relevance of answers based on the provided questions and images.

### Subtask 2: Synthetic Image Quality

-   **Subjective Evaluation**: Expert reviewers will assess realism and diagnostic utility.
-   **Objective Evaluation**:
    -   **Fréchet Inception Distance (FID)**: Measures the similarity between synthetic and real image distributions.
    -   **Structural Similarity Index Measure (SSIM)**: Quantifies structural resemblance to real images.

## Online Leaderboard

An online leaderboard will display participants' performance in real-time, encouraging iterative improvements and fostering competition.

## Preliminary Schedule

-   **20 December 2024**: Registration opens.
-   **14 February 2025**: Release of the training and validation datasets.
-   **14 March 2025**: Release of the test datasets.
-   **25 April 2025**: Registration closes.
-   **10 May 2025**: Run submission deadline.
-   **17 May 2025**: Release of processed results by the task organizers.
-   **30 May 2025**: Submission of participant papers [CEUR-WS].
-   **27 June 2025**: Notification of acceptance.
-   **7 July 2025**: Camera-ready copy of participant papers and extended lab overviews [CEUR-WS].
-   **9-12 September 2025**: CLEF 2025, Madrid, Spain.

## Organizers

-   **Steven A. Hicks** (steven@simula.no), SimulaMet, Norway
-   **Michael A. Riegler** (michael@simula.no), SimulaMet, Norway
-   **Vajira Thambawita** (vajira@simula.no), SimulaMet, Norway
-   **Pål Halvorsen** (paalh@simula.no), SimulaMet, Norway
-   **Sushant Gautam** (sushant@simula.no), SimulaMet, Norway

For further details and registration, visit: [https://www.imageclef.org/2025](https://www.imageclef.org/2025).
