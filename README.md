# 🌟 **ImageCLEFmed-MEDVQA-GI-2025** 🌟

📝 [**Registraion**](https://www.imageclef.org/2025#registration) | 📋 [View Registered Submissions](https://simulamet-medvqa.hf.space)

The [**ImageCLEFmed-MEDVQA-GI**](https://www.imageclef.org/2025/medical/vqa) (3rd edition) challenge 🔬 focuses on integrating **Visual Question Answering (VQA)** with **synthetic gastrointestinal (GI) data** 🏥 to enhance **diagnostic accuracy** 🏃‍♂️💡 and **AI learning algorithms** 🤖.  

This year's challenge includes **two exciting subtasks** 🚀 designed to push the boundaries of **image analysis** 🖼️ and **synthetic medical image generation** 🧬, aiming to improve **diagnostic processes** 🏨 and **patient outcomes** 💖.

---

## 🎯 **Task Descriptions**  

### 🔍 **Subtask 1: Algorithm Development for Question Interpretation and Response**  
💡 **Goal:** This subtask requires participants to develop AI models capable of accurately interpreting and answering clinical questions based on gastrointestinal (GI) images from the Kvasir-VQA dataset. The dataset consists of 6,500 annotated images covering a range of conditions and medical instruments. Questions are categorized into six types: Yes/No, Single-Choice, Multiple-Choice, Color-Related, Location-Related, and Numerical Count, necessitating the processing of both visual and textual information. Model performance will be evaluated using multiple quantitative metrics. 

✨ **Focus:** Create robust systems that combine **image** 🖼️ and **text understanding** 🗨️ to assist medical diagnostics 🏨.

#### 💬 **Example Questions:**  
- 🔢 *How many polyps are in the image?*  
- ⚡ *Are there any abnormalities in the image?*  
- 🏷️ *What disease is visible in the image?*  


#### 💥 Example Training Notebook: [Demo with HuggingFace Trainer](https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_1_Sample_Notebook.ipynb), [Demo with SWIFT CLI](https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_1_with_ms_swift_Sample_Notebook.ipynb)
---

### 🎨 **Subtask 2: Creation of High-Fidelity Synthetic GI Images**  
🖌️ **Goal:** Generate **synthetic GI images** 🧬 that are **indistinguishable** from real medical images 🏥, rich in detail and variability.  

🌱 **Why?** Provide **privacy-preserving alternatives** 🔒 to real patient data and **support diagnostic systems** 💡.
#### 💥 Example Training Notebook: [Demo with HuggingFace Diffusers](https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_2_with_diffusers_Sample_Notebook.ipynb)
---

## 📂 **Data**  
The 2025 dataset 🗃️ is an **extended version** of the **HyperKvasir dataset** 🔗 ([datasets.simula.no/hyper-kvasir](https://datasets.simula.no/hyper-kvasir)) and includes:
- 🏥 More **images** [(from KVASIR-VQA)](https://datasets.simula.no/kvasir-vqa/) than previous years with detailed **VQA annotations** simulating realistic diagnostic scenarios  📝  
- 🎯 [**Synthetically generated captions**](https://raw.githubusercontent.com/simula/ImageCLEFmed-MEDVQA-GI-2025/refs/heads/main/kvasir-captions.json) that can be used for image generation task. 🛠️   

### 📥 **Datasets**  
- 🏃 **Development Dataset:** [Kvasir-VQA](https://huggingface.co/datasets/SimulaMet-HOST/Kvasir-VQA) and [captions](https://raw.githubusercontent.com/simula/ImageCLEFmed-MEDVQA-GI-2025/refs/heads/main/kvasir-captions.json).
- 🕑 **Test Dataset:** *Coming Soon* ⏳  You can split the training dataset for model development now.

---

## 🧪 **Evaluation Methodology**  

### 🏃 **Subtask 1: Question Interpretation and Response**  
- 📊 **Metrics:** 🎯 *Accuracy*, 🔍 *Precision*, ♻️ *Recall*, and 🏆 *F1 Score*.  
- 📜 **Evaluation:** Based on **correctness** ✅ and **relevance** 📝 of answers using the provided **questions** 💬 and **images** 🖼️.

---

### 🖼️ **Subtask 2: Synthetic Image Quality**  
- 👀 **Subjective Evaluation:** 🩺 *Expert reviewers* will assess **realism** 🌟 and **diagnostic utility** 🏥.  
- 🎯 **Objective Evaluation:**  
  - 📉 **Fréchet Inception Distance (FID):** Similarity between synthetic and real images.  
  - 🏗️ **Structural Similarity Index Measure (SSIM):** Resemblance in structure 🏛️.
---

## 🏆 **Submission System**  
🚀 [View Registered Submissions](https://simulamet-medvqa.hf.space)

We use the [`medvqa`](https://pypi.org/project/medvqa/) Python package to **validate and submit** models to the official system.
The model that needs to be submiited is expected to be in a HuggingFace repository.

### 📦 Installation  
```bash
pip install -U medvqa
```
> The library is under **active development**. Always ensure you're using the **latest version**.

Your HuggingFace repo **must include** a standalone script named:
- [`submission_task1.py`](https://raw.githubusercontent.com/SushantGautam/MedVQA/refs/heads/main/medvqa/submission_samples/gi-2025/submission_task1.py) for Task 1  
- [`submission_task2.py`](https://raw.githubusercontent.com/SushantGautam/MedVQA/refs/heads/main/medvqa/submission_samples/gi-2025/submission_task2.py) for Task 2  

Use the provided **template script**, and make sure to:
- Modify all `TODO` sections  
- Add required information directly in the script

### ✅ Validate Before Submitting  
First make sure your submission script works fine in your working environment and it loads the model correctly from your submission repo and generates outputs in the required format.

```bash
python submission_task1.py
```

Next, you can validate the script to work independently. You can try it in a new venv:
```bash
medvqa validate --competition=gi-2025 --task=1/2 --repo_id=<your_repo_id>
```
- `--competition`: Set to `gi-2025`
- `--task`: Use `1` for Task 1 or `2` for Task 2  
- `--repo_id`: Your **HuggingFace model repo ID** (e.g., `SushantGautam/XXModelCheckpoint`)
- 
#### 📄 Additional Dependencies  
If your code requires extra packages, you must include a `requirements.txt` in the **root of the repo**. The system will install these automatically during validation/submission.
Else you will get package missing errors.

### 🚀 Submission Command  
If validation is okey, you can just run:
```bash
medvqa validate_and_submit --competition=gi-2025 --task=1/2 --repo_id=<your_repo_id>
```
This will make a submisision and your username, along with the task and time, should be visible on [the portal](https://simulamet-medvqa.hf.space) for it to be considered officially submitted.
The submission library will make your Hugging Face repository public but gated, granting the organizers access to your repo.
It must remain unchanged at least until the results of the competition are announced. However, you are free to make your model public. 

If you encounter any issues with submission, **don’t hesitate to contact us**.

---

## 🗓️ **Preliminary Schedule**  

- 📅 **20 December 2024:** 📝 *Registration opens*  
- 📅 **14 February 2025:** 🏃 *Release of training & validation datasets*  
- 📅 **9 April 2025:** ⏳ *Test datasets released*  
- 📅 **25 April 2025:** 🚪 *Registration closes*  
- 📅 **10 May 2025:** ⏲️ *Run submission deadline*  
- 📅 **17 May 2025:** 🏆 *Processed results released*  
- 📅 **30 May 2025:** ✍️ *Participant papers submission [CEUR-WS]*  
- 📅 **27 June 2025:** 💌 *Notification of acceptance*  
- 📅 **7 July 2025:** 🖨️ *Camera-ready paper submission [CEUR-WS]*  
- 🏛️ **9-12 September 2025:** 🌍 *CLEF 2025, Madrid, Spain 🇪🇸*  

---

## 💼 **Organizers**  
✨ For any queries, feel free to reach out to our amazing team:  
- 👨‍🔬 **Steven A. Hicks** 📧 [steven@simula.no](mailto:steven@simula.no)  
- 🧑‍💻 **Michael A. Riegler** 📧 [michael@simula.no](mailto:michael@simula.no)  
- 🧑‍🔬 **Vajira Thambawita** 📧 [vajira@simula.no](mailto:vajira@simula.no)  
- 👨‍🏫 **Pål Halvorsen** 📧 [paalh@simula.no](mailto:paalh@simula.no)  
- 🧑‍🎓 **[Sushant Gautam](http://sushant.info.np)** 📧 [sushant@simula.no](mailto:sushant@simula.no)  

---

## 🔗 **For More Details & Registration**  
📝 Visit:  👉 [**imageclef.org/2025#registration**](https://www.imageclef.org/2025#registration) 

📋 View Registered Submissions: 👉 [simulamet-medvqa.hf.space](https://simulamet-medvqa.hf.space)


💥 *Join the challenge, push the boundaries, and make a difference in medical AI!* 🚀🧬
