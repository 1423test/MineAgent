# MineAgent: Towards Remote-Sensing Mineral Exploration with Multimodal Large Language Models

MineBench is a Visual Question-Answering (VQA) dataset designed for mineral deposit exploration using multimodal large language models (MLLMs). The dataset comprises 612 geological areas (73 positive, 539 negative).

MineBench provides a unique challenge to MLLMs where both multi-image reasoning and long-tail domain understanding are required to accomplish one task.


## ⚡ Examples

### Example of MineBench
<img width="1033" alt="image" src="https://github.com/user-attachments/assets/dcab0064-dce7-4f5f-a59d-a971853d5dbf" />

To identify real-world mineral deposits, MineBench uses synthetic mineral patterns, as shown above. The exploration process involves four images: one geological image and three hyperspectral images. The synthetic mineral patterns are evaluated based on two key criteria for identifying mineral deposits:

1.**Spatial Consistency**: This criterion ensures that the colored regions across the three hyperspectral images show smooth spatial transitions, reflecting the gradual and continuous distribution of mineral deposits.

2.**Geological Alignment**: This criterion ensures that the colored regions in the hyperspectral images accurately correspond to the geological context presented in the geological image.

### Mineral pattern visualization

<img width="911" alt="image" src="https://github.com/user-attachments/assets/86583c37-7b7b-4290-9b56-809983ba835f" />

To visually represent real-world deposits alongside synthetic mineral patterns, the diagram above illustrates this comparison. Authentic deposit locations are marked with red points, which generally correspond to the synthetic color-coded regions.

**Positive samples**:  These samples show a smooth gradient of color transitions from red to yellow to orange, systematically capturing the alteration zones typically associated with fully developed mineral deposits. This pattern reflects the ongoing mineralization process.

**Negative samples**: These samples exhibit distinct characteristics, such as low color intensity (indicating minimal mineralization potential) or incomplete color transitions, suggesting that the deposit is in an early or incomplete stage of formation.


## 💭 Data Source
Remote sensing images: [Geoscience Australia ASTER Database](https://data.dea.ga.gov.au/?prefix=ASTER_Geoscience_Map_of_Australia/)

Deposit location labels [SARIG](https://map.sarig.sa.gov.au/), as illustrated below
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/0ef3aff3-6f62-4934-a197-a21247fb3064" />

## 💭 QA Pairs Construction
To enable MLLMs to directly evaluate on MineBench, the image-label pairs were converted into a Visual Question-Answering (VQA) format. The process involves the following steps:

1.**Task Definition**: Mineral exploration is framed as a binary classification problem, assessing deposit likelihood.

2.**Exploration Context**: Three instructions were manually assigned to each area to guide MLLM responses.

3.**Final Dataset**: The dataset consists of VQA pairs with multiple images, one question, and two answer options.


## 📚 Data

Here is a list of what has been released:

1. **QA Pairs for 612 Geological Areas**:  Image-label pairs have been converted into VQA (Visual Question Answering) pairs for exploratory analysis, access from [URL](https://drive.google.com/drive/folders/16K5_p6xAChraZKV3mGJTTzskX-fG_2H).
   
2. **Labeled deposit locations with mineral pattern visualization**: Authentic deposit locations are clearly marked on the images to indicate mineral patterns, access from [URL](https://drive.google.com/drive/folders/1bHUARAOXnXZH6lSp15aFZHy1Z4UYDUXC).
   
3. **Processed Image Download Links**: Users can download [them](https://drive.google.com/drive/folders/16K5_p6xAChraZKV3mGJTTzskX-fG_2H) to specified directories.







