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

---

### 🎨 **Subtask 2: Creation of High-Fidelity Synthetic GI Images**  
🖌️ **Goal:** Generate **synthetic GI images** 🧬 that are **indistinguishable** from real medical images 🏥, rich in detail and variability.  

🌱 **Why?** Provide **privacy-preserving alternatives** 🔒 to real patient data and **support diagnostic systems** 💡.

---

## 📂 **Data**  
The 2025 dataset 🗃️ is an **extended version** of the **HyperKvasir dataset** 🔗 ([datasets.simula.no/hyper-kvasir](https://datasets.simula.no/hyper-kvasir)) and includes:
- 🏥 More [**GI image data**](https://datasets.simula.no/kvasir-vqa/) than previous years with detailed **VQA annotations** simulating realistic diagnostic scenarios  📝  
- 🎯 [**Synthetically generated captions**]([https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/kvasir-captions.json](https://raw.githubusercontent.com/simula/ImageCLEFmed-MEDVQA-GI-2025/refs/heads/main/kvasir-captions.json)) that can be used for image generation task. 🛠️  

### 📥 **Datasets**  
- 🏃 **Development Dataset:** [Download Here](https://huggingface.co/datasets/SimulaMet-HOST/Kvasir-VQA)  
- 🕑 **Test Dataset:** *Coming Soon* ⏳  

---

## 🧪 **Evaluation Methodology**  

### 🏃 **Subtask 1: Question Interpretation and Response**  
- 📊 **Metrics:** 🎯 *Accuracy*, 🔍 *Precision*, ♻️ *Recall*, and 🏆 *F1 Score*.  
- 📜 **Evaluation:** Based on **correctness** ✅ and **relevance** 📝 of answers using the provided **questions** 💬 and **images** 🖼️.

#### 💥 Example Training Notebook: [Demo with HuggingFace Trainer](https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_1_Sample_Notebook.ipynb), [Demo with SWIFT CLI](https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_1_with_ms_swift_Sample_Notebook.ipynb)
---

### 🖼️ **Subtask 2: Synthetic Image Quality**  
- 👀 **Subjective Evaluation:** 🩺 *Expert reviewers* will assess **realism** 🌟 and **diagnostic utility** 🏥.  
- 🎯 **Objective Evaluation:**  
  - 📉 **Fréchet Inception Distance (FID):** Similarity between synthetic and real images.  
  - 🏗️ **Structural Similarity Index Measure (SSIM):** Resemblance in structure 🏛️.
#### 💥 Example Training Notebook: [Demo with HuggingFace Diffusers]([https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_1_with_ms_swift_Sample_Notebook.ipynb](https://github.com/simula/ImageCLEFmed-MEDVQA-GI-2025/blob/main/Task_2_with_diffusers_Sample_Notebook.ipynb))
---

## 🏆 **Online Leaderboard**  
🚀 Compete in **real-time** with a **dynamic leaderboard** 📈 showing participants' performance!  
💡 *Iterate, Improve & Win!* 🏅

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
