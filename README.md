# Malaria Classification with Neural Networks

## Motivation for Tackling the Malaria Problem

Malaria remains a critical public health issue, especially in tropical countries where resources are limited. By developing a neural network to analyze malaria data, we can support faster and more accurate diagnosis, ultimately reducing the burden on healthcare systems and saving lives.

---

## Information About Malaria

Malaria is a life-threatening disease spread to humans by some types of mosquitoes and is predominantly found in tropical countries. It is both preventable and curable. The infection is caused by a parasite and does not spread directly from person to person.

**Symptoms:**

- **Mild Symptoms:** Fever, chills, and headache.
- **Severe Symptoms:** Fatigue, confusion, seizures, and difficulty breathing.

Certain groups, including infants, children under 5 years, pregnant women, travelers, and people with HIV or AIDS, are at a higher risk of severe infection. Malaria transmission occurs through the bite of an infected mosquito, which introduces the parasites into the bloodstream. These parasites then infect primarily the liver cells and red blood cells, where they complete part of their life cycle.

---

## Key Facts and Big Numbers

- **Global Impact (2023):**
  - **263 million** estimated malaria cases.
  - **597,000** estimated malaria deaths across **83 countries**.
- **WHO African Region:**
  - Accounts for **94%** of malaria cases (approximately **246 million** cases).
  - Responsible for **95%** of malaria deaths (approximately **569,000** deaths).
  - Children under 5 years old represent about **76%** of all malaria deaths in the region.

---

## Definition of the Problem

The primary objective is the **classification of a cell** as either infected with malaria or not infected. This classification task is crucial in facilitating timely and accurate treatment decisions.

I used a dataset from TensorFlow based on the Data Collection and Preparation as described below: https://www.tensorflow.org/datasets/catalog/malaria

---

## Data Collection and Preparation

To reduce the workload for microscopists in resource-constrained regions and improve diagnostic accuracy, researchers at the Lister Hill National Center for Biomedical Communications (LHNCBC) have developed a mobile application. This application runs on a standard Android® smartphone attached to a conventional light microscope. Key details of the data collection process include:

- **Data Acquisition:**
  - Giemsa-stained thin blood smear slides were used.
  - Slides were collected from **150 P. falciparum-infected** patients and **50 healthy** patients at Chittagong Medical College Hospital, Bangladesh.
  - Images were captured using the smartphone's built-in camera for each microscopic field of view.
- **Annotation and Archival:**
  - An expert slide reader at the Mahidol-Oxford Tropical Medicine Research Unit in Bangkok, Thailand, manually annotated the images.
  - The de-identified images and annotations are archived at the National Library of Medicine (NLM) under IRB#12972.
- **Image Processing:**
  - A level-set based algorithm was applied to detect and segment the red blood cells.
- **Dataset Composition:**
  - The final dataset comprises **27,558 cell images**.
  - There is an equal representation of parasitized (positive) and uninfected (negative) cell images.
  - Positive samples contain _Plasmodium_ parasites, while negative samples include other objects such as staining artifacts or impurities.

---

## Notebook Overview

This Jupyter Notebook contains the full workflow of the project, including:

- Data loading and preprocessing
- Model building and architecture design
- Training and evaluation of the neural network
- Visualization of results and performance metrics

The notebook is documented with comments and markdown cells to help you understand each step of the process.

---

## Getting Started

To start using this project, follow these steps:

1. **Clone the Repository:**

   ```bash
   git clone <https://github.com/tiagoAG28/malaria_CNN/blob/main>
   cd <malaria_CNN.ipynb>

   ```

2. **Install Dependencies:**

Ensure you have Python 3.x installed. Then install the required packages using pip:

pip install tensorflow numpy matplotlib pandas jupyter

3. **Launch the Notebook:**

Start Jupyter Notebook or Jupyter Lab:

Open the notebook file, malaria_CNN.ipynb, and run the cells sequentially.

4. **Explore and Modify:**

The notebook is organized in a step-by-step manner. Feel free to modify the code and parameters to experiment with different model architectures or hyperparameters.

---


# Conclusion

By harnessing the power of deep learning, this project aims to provide a robust and scalable tool for the classification of malaria-infected cells. The ultimate goal is to enhance diagnostic efficiency and accuracy, particularly in regions that are most affected by malaria, thereby contributing to better health outcomes and a reduction in the global malaria burden.

---


# Future Work

- **Additional Metrics:**  
  Integrate further evaluation metrics such as recall, precision, and F1 score to provide a more comprehensive performance analysis of the model.

- **Confusion Matrix:**  
  Develop and explain a confusion matrix to visualize and better understand the model's classification performance. A confusion matrix displays the counts of true positives, true negatives, false positives, and false negatives, offering insight into potential biases or areas for improvement.

- **Deployment:**  
  Deploy the model to a web application (e.g., using Streamlit) to make it accessible for real-time predictions and facilitate user interaction.

- **Model Optimization:**  
  Explore additional techniques like hyperparameter tuning, data augmentation, and advanced regularization to further improve the model’s performance.

---


**Sources:**

https://pmc.ncbi.nlm.nih.gov/articles/PMC5907772/

https://www.who.int/news-room/fact-sheets/detail/malaria
