# MineAgent: Towards Remote-Sensing Mineral Exploration with Multimodal Large Language Models

## ⚡ Introduction
MineBench is a VQA dataset consisting of 612 geological areas, which we hope will  aid in exploring mineral deposit through multimodal large language models (MLLMs).
The resulting dataset consists of 73 positive areas and 539 negative areas

MineBench provides a unique challenge to MLLMs where both multi-image reasoning and long-tail domain understanding are required to accomplish one task.

## Example of MineBench
The real deposit with synthetic mineral patterns:
<img width="911" alt="image" src="https://github.com/user-attachments/assets/86583c37-7b7b-4290-9b56-809983ba835f" />
The authentic deposit locations (marked in red points) predominantly align with synthetic color-coded regions. 
Positive samples exhibit a gradual color transition from red to yellow to orange, systematically capturing the alteration zone characteristic of complete mineral deposits and reflecting the continuous mineralization processes. In contrast, negative samples display markedly different characteristics, with either low color intensity indicating minimal mineralization potential or an absence of complete color transitions suggesting incomplete deposit formation.

Standrad MineBench to explore the mineral patterns:



the Geologocal context align with the colored area in the altertion zones, more the three altertion zones with the smooth spatial transition.

Here is a list of what has been released:

1. **QA Pairs for 612 Geological Areas**: Images-label pairs converted into VQA pairs for exploring.
2. **Real deposit marking**: we mark the real deposit in the images to show the mineral patterns.
3. **Precossed Image Download Links**: Users can download them to specified directories.

## 💭 Data Source
We access the remote-sensing imaging directly sourced from [Geoscience](https://data.dea.ga.gov.au/?prefix=ASTER_Geoscience_Map_of_Australia/)
We access the deposit locations directly sourced from authoritative records as class labels
from [SARIG](https://map.sarig.sa.gov.au/), the deposit location is shown as the following.
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/0ef3aff3-6f62-4934-a197-a21247fb3064" />

## 💭 QA Pairs Construction
To enable MLLMs to directly evaluate on MineBench, the image-label pairs were converted into a Visual Question-Answering (VQA) format. The process involves the following steps:
1. **Task Definition**: Each area was manually assigned 3 instructions to guide the MLLM in answering the task related to the area.
2. Mineral exploration enables quantifiable assessments of deposit likelihood, facilitating prioritization of exploration areas, so it is usually formulated as a binary classification problem. 
3. **Conversion to VQA Format**: All image-label pairs were converted into single-choice questions with binary classfication.
4. **Final Dataset**: The resulting dataset consisted of VQA pairs, where multiple images are paired with a question and four options, one of which is correct.


## 📚 Data

You can access the QA pairs of MineBench.
The tables below record the download URLs for the images from [URL](https://drive.google.com/drive/folders/16K5_p6xAChraZKV3mGJTTzskX-fG_2H_).
And you can see the real deposit location and the mineal pattern in [URL](https://drive.google.com/drive/folders/1bHUARAOXnXZH6lSp15aFZHy1Z4UYDUXC)



