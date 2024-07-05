<p align="left">
    English</a>&nbsp ｜ &nbsp<a href="README_CN.md">中文</a>&nbsp
</p>
<br><br>

<p align="center">
    <img src="imgs/logo.png" width="400"/>
<p>
<br>


<div align="center">
  <a href='https://huggingface.co/Kwai-Kolors/Kolors'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-yellow'></a> &ensp;
  <a href="https://github.com/Kwai-Kolors/Kolors"><img src="https://img.shields.io/static/v1?label=Kolors Code&message=Github&color=blue&logo=github-pages"></a> &ensp;
  <a href="https://kwai-kolors.github.io/"><img src="https://img.shields.io/static/v1?label=Team%20Page&message=Page&color=green"></a> &ensp;

  <a href="https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/Kolors_paper.pdf"><img src="https://img.shields.io/static/v1?label=Tech Report&message=Arxiv:Kolors&color=red&logo=arxiv"></a> &ensp;
  <a href="https://kolors.kuaishou.com/"><img src="https://img.shields.io/static/v1?label=Official Website&message=Page&color=green"></a> &ensp;
</div>



# Kolors: Effective Training of Diffusion Model for Photorealistic Text-to-Image Synthesis
<figure>
  <img src="imgs/head_final3.png">
</figure>
<br><br>

## Contents

- [🎉 News](#News)
- [📑 Open-source Plan](#open-source-plan)
- [📖 Introduction](#Introduction)
- [📊 Evaluation 🥇🥇🔥🔥](#Evaluation)
- [🎥 Visualization](#Visualization)
- [🛠️ Usage](#Usage)
- [📜 License & Citation & Acknowledgments](#License)
<br><br>


## <a name="News"></a>🎉 News
* 2024.07.06 🔥🔥🔥 We release **Kolors**, a large text-to-image model trained on billions of text-image pairs. This model is bilingual in both Chinese and English, and supports a context length of 256 tokens. For more technical details, please refer to [technical report](https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/Kolors_paper.pdf).
* 2024.07.03 📊 Kolors won the second place on [FlagEval Multimodal Text-to-Image Leaderboard](https://flageval.baai.ac.cn/#/leaderboard/multimodal?kind=t2i), excelling particularly in the Chinese and English subjective quality assessment where Kolors took the first place.
* 2024.07.02 🎉 Congratulations! Our paper on controllable video generation, [DragAnything: Motion Control for Anything using Entity Representation](https://arxiv.org/abs/2403.07420), have been accepted by ECCV 2024.
* 2024.02.08 🎉 Congratulations! Our paper on generative model evaluation, [Learning Multi-dimensional Human Preference for Text-to-Image Generation](https://wangbohan97.github.io/MPS/), have been accepted by CVPR 2024.
<br><br>

## <a name="open-source-plan"></a>📑 Open-source Plan

- Kolors (Text-to-Image Model)
  - [x] Inference 
  - [x] Checkpoints 
  - [ ] LoRA
  - [ ] ControlNet (Pose, Canny, Depth)
  - [ ] IP-Adapter
- [ ] ComfyUI
- [ ] Diffusers
<br><br>

## 
## <a name="Introduction"></a>📖 Introduction

Kolors is a large-scale text-to-image generation model based on latent diffusion, developed by the Kuaishou Kolors team. Trained on billions of text-image pairs, Kolors exhibits significant advantages over both open-source and closed-source models in visual quality, complex semantic accuracy, and text rendering for both Chinese and English characters. Furthermore, Kolors supports both Chinese and English inputs, demonstrating strong performance in understanding and generating Chinese-specific content. For more details, please refer to this <a href="https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/Kolors_paper.pdf">technical report</a></b>.
<br><br>

## <a name="Evaluation"></a>📊 Evaluation
We have collected a comprehensive text-to-image evaluation dataset named KolorsPrompts to compare Kolors with other state-of-the-art open models and closed-source models. KolorsPrompts includes over 1,000 prompts across 14 catagories and 12 evaluation dimensions. The evaluation process incorporates both human and machine assessments. In relevant benchmark evaluations, Kolors demonstrated highly competitive performance, achieving industry-leading standards.

<br><br>

### Human Assessment

For the human evaluation, we invited 50 imagery experts to conduct comparative evaluations of the results generated by different models. The experts rated the generated images based on three criteria: visual appeal, text faithfulness, and overall satisfaction. In the evaluation, Kolors achieved the highest overall satisfaction score and significantly led in visual appeal compared to other models.

|       Model       | Average Overall Satisfaction | Average Visual Appeal | Average Text Faithfulness |
| :--------------: | :--------: | :--------: | :--------: |
|  Adobe-Firefly   |    3.03    |    3.46    |    3.84    |
| Stable Diffusion 3 |    3.26    |    3.50    |    4.20    |
|     DALL-E 3      |    3.32    |    3.54    |    4.22    |
|  Midjourney-v5   |    3.32    |    3.68    |    4.02    |
| Playground-v2.5  |    3.37    |    3.73    |    4.04    |
|  Midjourney-v6   |    3.58    |    3.92    |    4.18    |
|    **Kolors**    |    **3.59**    |    **3.99**    |    **4.17**    |

------

<div style="color: gray; font-size: small;">

**All model results are tested with the April 2024 product versions**

</div>
<br>

### Machine Assessment
We used [MPS](https://arxiv.org/abs/2405.14705) (Multi-dimensional Human Preference Score) on KolorsPrompts as the evaluation metric for machine assessment. Kolors achieved the highest MPS score, which is consistent with the results of the human evaluations.

<div style="text-align:center">

| Models            | Overall MPS |
|:-------------------:|:-------------:|
| Adobe-Firefly     | 8.5     |
| Stable Diffusion 3  | 8.9      |
| DALL-E 3           |   9.0    |
| Midjourney-v5     | 9.4      |
| Playground-v2.5   | 9.8      |
| Midjourney-v6     | 10.2      |
| **Kolors**        | **10.3**      |
</div>


<br>

For more experimental results and details, please refer to our [technical report](https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/Kolors_paper.pdf).

<br><br>


## <a name="Visualization"></a>🎥 Visualization

* **High-quality Portrait**
<div style="display: flex; justify-content: space-between;">
  <img src="imgs/zl8.png" />
</div>
<br>

* **Chinese Elements Generation**
<div style="display: flex; justify-content: space-between;">
  <img src="imgs/cn_all.png"/>
</div>
<br>

* **Complex Semantic Understanding**
<div style="display: flex; justify-content: space-between;">
  <img src="imgs/fz_all.png"/>
</div>
<br>

* **Text Rendering**
<div style="display: flex; justify-content: space-between;">
  <img src="imgs/wz_all.png" />
</div>
<br>
</div>

The visualized case prompts mentioned above can be accessed [here](https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/prompt_vis.txt). 
<br><br>

## <a name="Usage"></a>🛠️ Usage

### Requirements

* Python 3.8 or later
* PyTorch 1.13.1 or later
* Transformers 4.26.1 or later
* Recommended: CUDA 11.7 or later
<br>

1. Repository Cloning and Dependency Installation

```bash
apt-get install git-lfs
git clone https://github.com/Kwai-Kolors/Kolors
cd Kolors
conda create --name kolors python=3.8
conda activate kolors
pip install -r requirements.txt
python3 setup.py install
```
2. Weights download（[link](https://huggingface.co/Kwai-Kolors/Kolors)）：
```bash
git lfs clone https://huggingface.co/Kwai-Kolors/Kolors weights/Kolors
```
3. Inference：
```bash
python3 scripts/sample.py "一张瓢虫的照片，微距，变焦，高质量，电影，拿着一个牌子，写着“可图”"
# The image will be saved to "scripts/outputs/sample_text.jpg"
```
<br><br>

## <a name="License"></a>📜 License & Citation & Acknowledgments

### License

Kolors are fully open-sourced for academic research. For commercial use, please fill out this [questionnaire](https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/可图KOLORS模型商业授权申请书.docx) and sent it to kwai-kolors@kuaishou.com for registration.
 
We open-source Kolors to promote the development of large text-to-image models in collaboration with the open-source community. The code of this project is open-sourced under the Apache-2.0 license. We sincerely urge all developers and users to strictly adhere to the [open-source license](MODEL_LICENSE), avoiding the use of the open-source model, code, and its derivatives for any purposes that may harm the country and society or for any services not evaluated and registered for safety. Note that despite our best efforts to ensure the compliance, accuracy, and safety of the data during training, due to the diversity and combinability of generated content and the probabilistic randomness affecting the model, we cannot guarantee the accuracy and safety of the output content, and the model is susceptible to misleading. This project does not assume any legal responsibility for any data security issues, public opinion risks, or risks and liabilities arising from the model being misled, abused, misused, or improperly utilized due to the use of the open-source model and code.

### Citation
If you find our work helpful, please cite it!

```
@article{kolors,
  title={Kolors: Effective Training of Diffusion Model for Photorealistic Text-to-Image Synthesis},
  author={Kolors Team},
  journal={arXiv preprint},
  year={2024}
}
```

### Acknowledgments
- Thanks to [Diffusers](https://github.com/huggingface/diffusers) for providing the codebase.
- Thanks to [ChatGLM3](https://github.com/THUDM/ChatGLM3) for providing the powerful Chinese language model.
<br>

### Contact Us

If you want to leave a message for our R&D team and product team, feel free to join our [WeChat group](https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/wechat.png). You can also contact us via email (kwai-kolors@kuaishou.com).

[![Star History Chart](https://api.star-history.com/svg?repos=Kwai-Kolors/Kolors&type=Date)](https://star-history.com/#Kwai-Kolors/Kolors&Date)
