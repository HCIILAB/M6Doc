# M<sup>6</sup>Doc_Dataset_Release

<p align="center">
    <a href="https://openaccess.thecvf.com/content/CVPR2023/papers/Cheng_M6Doc_A_Large-Scale_Multi-Format_Multi-Type_Multi-Layout_Multi-Language_Multi-Annotation_Category_Dataset_CVPR_2023_paper.pdf"><img src="https://img.shields.io/badge/Paper-PDF-orange.svg" alt="PDF"></a>
    <a href="https://huggingface.co/datasets"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Dataset-yellow.svg" alt="Hugging Face"></a>
    <a href="README_zh.md"><img src="https://img.shields.io/badge/语言-中文版-blue.svg" alt="Chinese Version"></a>
</p>

The [M<sup>6</sup>Doc](https://openaccess.thecvf.com/content/CVPR2023/html/Cheng_M6Doc_A_Large-Scale_Multi-Format_Multi-Type_Multi-Layout_Multi-Language_Multi-Annotation_Category_Dataset_CVPR_2023_paper.html) dataset for the research of document layout analysis in Modern Document is released by the Deep Learning and Visual Computing Lab of South China University of Technology.

---

## Dataset Download

| Platform | Link | Details / Size | Password Required |
| :--- | :--- | :--- | :---: |
| **Hugging Face** | [🤗 Dataset Repository Files](https://huggingface.co/datasets) | Full dataset archives | **Yes** (encrypted archive) |
| **Baidu Cloud** | [Download via BaiduNetdisk](https://pan.baidu.com/s/1jV9WTE9yVZfwWF_x1JZE9Q?pwd=xx3k) | 12.45 GB (Extract Code: `xx3k`) | **Yes** (decompression password) |

---

## ⚠️ Access Request & Application Instructions

The M<sup>6</sup>Doc dataset can **only be used for non-commercial research purposes**. The dataset is publicly accessible but **encrypted with an additional password**. To request access, please follow these steps:

### Step 1: Download and complete the agreement document:
- 📄 [Application Form for Using M<sup>6</sup>Doc (Direct Download)](Application_Form/Application-Form-for-Using-M6Doc.docx)
- 📁 [Application_Form Directory](Application_Form/)

Have this document **signed and stamped** by your institution. Please also prepare **1–2 recent publications (within the last 6 years)** as evidence that you or your team conduct research in OCR, handwriting analysis and recognition, document image processing, or visual information extraction.

### Step 2: Submit your application online:
> 🔗 **[SCUT DLVC Lab Dataset Access Portal → Apply for M6Doc](http://121.41.49.212:9000/apply/m6doc)**

Upload both signed documents through the portal and fill out the "Recent Publications" block. Your application will be reviewed manually and you will be notified by email once a decision has been made (typically within 1–5 business days).

### Step 3: Decompress the dataset:
After approval, you will receive the decompression password via email.

> ⚠️ All users must comply with the use conditions at all times; failure to do so will result in revocation of access.

---

## License
The M<sup>6</sup>Doc dataset should be used and distributed under the [Creative Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/) for non-commercial research purposes.

---

## M<sup>6</sup>Doc Dataset Overview
The M<sup>6</sup>Doc dataset contains a total of 9,080 modern document images, which are categorized into seven subsets, *i.e.*, scientific article (11%), textbook (23%), test paper (22%), magazine (22%), newspaper (11%), note (5.5%), and book (5.5%) according to their content and layouts. It contains three formats: PDF (64%), photographed documents (5%), and scanned documents (31%). The dataset includes a total of 237,116 annotated instances. 

---

## Dataset Source
The M<sup>6</sup>Doc datasets were collected from various sources, including [arXiv](https://arxiv.org/), the official website of the [Chinese People's Daily](http://paper.people.com.cn/), and [VKontakte](https://vk.com/). The source and composition of different subsets are shown below:

* The **scientific article** subset includes articles obtained by searching with the keywords "Optical Character Recognition" and "Document Layout Analysis" on arXiv. PDF files were then downloaded and converted to images.
* The **textbook** subset contains 2,080 scanned document images from textbooks for three grades (elementary, middle, and high school) and nine subjects (Chinese, Math, English, Physics, Chemistry, Biology, History, Geography, and Politics).
* The **test paper** subset consists of 2,000 examination papers covering the same nine subjects as the textbook subset.
* The **magazine** subset includes 1,000 Chinese and English magazines in PDF format, respectively. The Chinese magazines were sourced from five publishers: *Global Science*, *The Mystery*, *Youth Digest*, *China National Geographic*, and *The Reader*. The English magazines were sourced from five American publishers: *The New Yorker*, *New Scientist*, *Scientific American*, *The Economist*, and *Time USA*.
* The **newspaper** subset contains 500 PDF document images from the *Chinese People's Daily* and the *Wall Street Journal*.
* The **note** subset consists of students' handwritten notes in nine subjects, including 500 scanned pages.
* The **book** subset contains 500 photographed images, which were acquired from 50 books with 10 pages each. Each book has a distinct layout, resulting in considerable diversity in this subset.

---

## Data Annotation

### Label Definition
To ensure that the definition of document layout elements is reasonable and traceable, we reviewed relevant information, such as layout knowledge and layout design. We also used knowledge from the book *"Page Design: New Layout & Editorial Design (2019)"* and referred to layout guidelines. In most cases, we followed the [Wikipedia](https://www.wikipedia.org) definition. Consequently, we defined 74 detailed document annotation labels. 

The key factors in selecting these annotation labels include (1) the commonality of annotation labels between different document types, (2) the specificity of labels between different document types, (3) the frequency of labels, and (4) the recognition of independent pages. Figure 1 shows annotation samples of M<sup>6</sup>Doc. There are a total of 74 annotation categories in our dataset.

![Example annotations of M6Doc](img/m6doc_example.png)
<p align="center">Figure 1. Example annotations of the M<sup>6</sup>Doc. Zoom in for better view.</p>

Table 2 summarizes the overall frequency and distribution of labels.

<p align="center">Table 2. M<sup>6</sup>Doc dataset overview.</p>

![M6Doc dataset overview](img/m6doc_dataset_review.png)

### Annotation Guideline
We provide a detailed annotation guideline ([guideline_chinese.pdf](guideline/guideline_chinese.pdf), over 170 pages) and some typical annotation examples. 47 annotators performed the annotation task strictly according to the guidelines.

---

## Directory Format
The dataset is organized in the following directory format:

```text
├── M6Doc
    ├── annotations
    │   ├── instances_train2017.json
    │   └── instances_val2017.json
    ├── train2017
    │   ├── xxx.jpg
    │   └── ...
    └── val2017
        ├── xxx.jpg
        └── ...
```

---

## Citation and Contact
Please consider to cite our paper when you use our dataset:

```bibtex
@InProceedings{Cheng_2023_CVPR,
    author    = {Cheng, Hiuyi and Zhang, Peirong and Wu, Sihang and Zhang, Jiaxin and Zhu, Qiyuan and Xie, Zecheng and Li, Jing and Ding, Kai and Jin, Lianwen},
    title     = {M6Doc: A Large-Scale Multi-Format, Multi-Type, Multi-Layout, Multi-Language, Multi-Annotation Category Dataset for Modern Document Layout Analysis},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2023},
    pages     = {15138-15147}
}
```

While this work primarily focuses on modern documents, we are also conducting research on the layout analysis of Ancient Chinese Books. Please refer to the [SCUT-CAB Dataset Release](https://github.com/HCIILAB/SCUT-CAB_Dataset_Release) and [guideline_Ancient](guideline/guideline_ancient.pdf) for more details.

For any questions about the dataset, please contact the authors by sending an email to Prof. Jin ([eelwjin@scut.edu.cn](mailto:eelwjin@scut.edu.cn), or [lianwen.jin@gmail.com](mailto:lianwen.jin@gmail.com)).
