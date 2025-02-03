<div align="center">
    
    
 <div>

<a href="https://github.com/Q-Future/"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fvqassessment%2FA-Bench&count_bg=%23E97EBA&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=visitors&edge_flat=false"/></a>
    <a href="https://github.com/Q-Future/A-Bench"><img src="https://img.shields.io/github/stars/Q-Future/A-Bench"/></a>
    <a href="https://arxiv.org/pdf/2406.03070"><img src="https://img.shields.io/badge/Arxiv-2406.03070-blue"/></a>
    <a href="https://huggingface.co/datasets/q-future/A-Bench"><img src="https://img.shields.io/badge/Data-Release-green"></a>
   </div>

  <div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="a-bench.png">
  </div>

<div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="teaser.jpg">
  </div>
  
  <h1>A-Bench: Are LMMs Masters at Evaluating AI-generated Images?</h1>
  
_What do we expect from LMMs as AIGI evaluators and how do they perform?_

  <div>
      <a href="https://zzc-1998.github.io/" target="_blank">Zicheng Zhang</a><sup>1</sup><sup>*</sup>,
      <a href="https://teowu.github.io/" target="_blank">Haoning Wu</a><sup>2</sup><sup>*</sup>,
      <a href="https://github.com/lcysyzxdxc" target="_blank">Chunyi Li</a><sup>1</sup><sup>*</sup>,
      <a href="https://scholar.google.com/citations?hl=zh-CN&user=85yWgIcAAAAJ" target="_blank">Yingjie Zhou</a><sup>1</sup>,
      <a href="https://scholar.google.com/citations?hl=zh-CN&user=nDlEBJ8AAAAJ" target="_blank">Wei Sun</a><sup>1</sup>,
  </div>

<div>
      <a href="https://minxiongkuo.github.io/" target="_blank">Xiongkuo Min</a><sup>1</sup>,
      <a href="https://scholar.google.com/citations?hl=zh-CN&user=NSR4UkMAAAAJ" target="_blank">Zijian Chen</a><sup>1</sup>,
      <a href="https://scholar.google.ca/citations?user=Tq2hoMQAAAAJ&hl=en" target="_blank">Xiaohong Liu</a><sup>1</sup>,
      <a href="https://personal.ntu.edu.sg/wslin/Home.html" target="_blank">Weisi Lin</a><sup>2</sup>,
      <a href="https://ee.sjtu.edu.cn/en/FacultyDetail.aspx?id=24&infoid=153&flag=153" target="_blank">Guangtao Zhai</a><sup>1</sup><sup>#</sup>
      
  </div>
  <div>
  <sup>1</sup>Shanghai Jiaotong University,  <sup>2</sup>Nanyang Technological University
       </div>   
<div>
<sup>*</sup>Equal contribution. <sup>#</sup>Corresponding author. 
   </div>
  <a href="https://github.com/Q-Future/A-Bench/blob/main/A_Bench__Are_LMMs_Masters_at_Evaluating_AI_generated_Images_.pdf"><strong>Paper</strong></a> |
<a href="https://a-bench-sjtu.github.io/"><strong>Project Page</strong></a> |
<a href="https://github.com/Q-Future/A-Bench"><strong>Github</strong></a> |
 <a href="https://huggingface.co/datasets/q-future/A-Bench"><strong>Data</strong></a> 
  <div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="spotlight.png">
  </div>
  
<div align="left">
    
T2I models aim to create images that accurately align with the text and showcase high perceptual quality. Therefore, the proposed A-Bench includes two parts to diagnose whether LMMs are masters at evaluating AIGIs: **1) Semantic Understanding, 2) Quality Perception**.
 


## Release
- [2025/1] 🔥**A-Bench** is accepted by ICLR 2025, and more recent LMMs' performance is added.
- [2024/9/26]🔥 Update the performance of GPT \& Gemini with the latest version on **A-Bench**.
- [2024/8/1]🔥 The **A-Bench** is released on [VLMEvalKit](https://github.com/open-compass/VLMEvalKit), come and test your LMM with one command.
- [2024/6/17]🔥 The **A-Bench** has now joined [lmms-eval](https://github.com/EvolvingLMMs-Lab/lmms-eval), which makes it easier to test LMM !!
- [2024/6/5] 🔥 We are releasing the **A-Bench** data and meta information at [Huggingface](https://huggingface.co/datasets/q-future/A-Bench).
- [2024/6/3] 🔥 [Github repo](https://github.com/Q-Future/A-Bench) for **A-Bench** is online. Do you want to find out if your LMM is a master at evaluating AI-generated images? Come and test on **A-Bench** !!

  
## A-Bench Construction
    
Two key diagnostic subsets are defined: **A-Bench-P1** → high-level semantic understanding, and **A-Bench-P2** → low-level quality perception. For high-level semantic understanding, **A-Bench-P1** targets three critical areas: *Basic Recognition, Bag-of-Words Pitfalls Discrimination*, and *Outside Knowledge Realization*, which are designed to progressively test the LMM’s capability in AIGI semantic understanding, moving from simple to complex prompt-related content. For low-level quality perception, **A-Bench-P2** concentrates on *Technical Quality Perception, Aesthetic Quality Evaluation*, and *Generative Distortion Assessment*, which are designed to cover the common quality issues and AIGI-specific quality problems. 

Specifically, a comprehensive dataset of 2,864 AIGIs sourced from various T2I models is compiled, including 1,408 AIGIs for **A-Bench-P1** and 1,456 for **A-Bench-P2**. Each AIGI is paired with a question-answer set annotated by human experts.
We are open to **submission-based evaluation** for **A-Bench**. The details for submission are in the **Evaluate your model on A-Bench** Section.

  <div style="width: 100%; text-align: center; margin:auto;">
      <img style="width:100%" src="examples.png">
  </div>

  
## Glance at A-Bench Performance
For *open-source* models, **LLaVA-NeXT (Qwen-110B)** takes the first place. For *closed-source* models, **GEMINI 1.5 PRO** takes the first place.

<div align="center">
<div style="width: 100%; text-align: center; margin:auto;">
  <img style="width:80%" src="overall.png">
</div>
    
**A Quick Look of the A-Bench Outcomes.**


|**Participant Name** | Major↑ | Minor↑ | Attr.↑ | N. Adj.↑ | Comp.↑ | Number↑ | Term↑ | Contra.↑ | Technical↑ | Aesthetic↑ | Generative↑ |
| - | - | - | - | - | - | -| - | - | - | - | - |
| Gemini 1.5 Pro | 93.82%   | 95.18%   | 94.35%   | 80.27%   | 72.14%   | 79.35%   | 72.88%   | 61.56%   | 84.70%   | 71.22%   | 77.61%   | 59.07%   | 69.12%   |
| GPT-4v | 92.95%   | 96.00%   | 87.40%   | 82.67%   | 64.39%   | 68.84%   | 77.60%   | 66.73%   | 83.60%   | 67.82%   | 68.34%   | 58.02%   | 64.31%   |
| GPT-4o | 94.34%   | 95.14%   | 91.99%   | 79.54%   | 76.40%   | 73.30%   | 77.47%   | 68.59%   | 85.44%   | 70.59%   | 61.61%   | 67.92%   | 66.88%   |
| Qwen-VL-Max | 92.56%   | 94.75%   | 91.99%   | 85.78%   | 68.94%   | 75.85%   | 78.94%   | 65.05%   | 84.47%   |  71.31%     | 69.77%   | 58.56%  |  66.21%   |
| Human (Worst) | 95.18%   | 94.24%   | 96.78%   | 88.70%   | 85.49%   | 82.46%   | 81.76%   | 88.91%   | 92.40%   | 94.32%   | 84.49%   | 86.25%   | 90.56%   |
| Human (Best) | 95.40%   | 95.21%   | 99.42%   | 95.17%   | 93.34%   | 91.73%   | 84.29%   | 96.05%   | 94.02%   | 94.69%   | 86.01%   | 93.00%   | 92.22%   |
<div align="left">  
    
We release the performance of top-tier *closed-source* LMMs against humans.
Two conclusions can be obtained: 
    
1) **LMMs excel at basic recognition tasks but tend to be less effective
when it comes to nuanced semantic understanding.**

2) **LMMs are poor quality evaluators.**


## Evaluate your model on A-Bench


### With LMMs-Eval


Use [LMMs-eval](https://github.com/EvolvingLMMs-Lab/lmms-eval) to automatically evaluate A-Bench:

```shell
git clone https://github.com/EvolvingLMMs-Lab/lmms-eval.git
cd lmms-eval
pip install -e .

export NUM_GPUS=8
export MODEL_NAME=idefics2
python3 -m accelerate.commands.launch --num_processes=$NUM_GPUS -m lmms_eval --model $MODEL_NAME --tasks abench_dev --batch_size 1 --log_samples --log_samples_suffix $MODEL_NAME_a_bench --output_path ./logs/
```

### With VLMEvalKit

Use [VLMEvalKit](https://github.com/open-compass/VLMEvalKit) to automatically evaluate A-Bench:

```
git clone https://github.com/open-compass/VLMEvalKit.git
cd VLMEvalKit
pip install -e .
```

Example, quick test InternVL2-1B on the val and test sets of A-Bench:

```
python run.py --data A-Bench_VAL A-Bench_TEST --model InternVL2-1B --verbose
```

The val set has the correct answers and you can directly get the acc results. For test set performance, please submit the results to [e-mail](zzc1998@sjtu.edu.cn)

### With ```datasets``` API

TO evaluate on your custom model, you can use our [converted dataset](https://huggingface.co/datasets/q-future/A-Bench-HF) in huggingface `datasets` format:

```shell
pip install datasets
```

```python
from datasets import load_dataset

ds = load_dataset("q-future/A-Bench-HF")
ds["dev"][0]
```

Outputs should be as follows:
```
{'id': 0,
 'image': <PIL.PngImagePlugin.PngImageFile image mode=RGB size=512x288>,
 'question': 'May I ask where the scene in the picture is located?',
 'option0': 'Forest',
 'option1': 'Riverside',
 'option2': 'Desert',
 'option3': 'N/A',
 'category': 'part1 -> bag_of_words -> attribute',
 'correct_choice': 'B'}
```

Which can be then evaluated with your own model's format for MCQ.

For example, if your model follows llava's format, it should be as follows:

```python
di = ds["dev"][0]
prompt = di["question"] + "\n"
for i in range(4):
    if di[f"option{i}"] != "N/A":
        prompt += chr(ord("A")+i) + ". " + di[f"option{i}"] + "\n"
prompt = prompt + "Answer with the option's letter from the given choices directly."

print(prompt)
```

The prompt for the previous data item should be ```May I ask where the scene in the picture is located?
A. Forest
B. Riverside
C. Desert
Answer with the option's letter from the given choices directly.```

### Legacy

First download the dataset and meta information from [Huggingface](https://huggingface.co/datasets/q-future/A-Bench).

The *imgs.zip* contains all the AI-generated images and *Abench.json* contains all the meta information including the img_path, questions, answers, and categories. The item of *Abench.json* is structured like:

```
"img_path": "part1_0000.png",
"question": "What is the color of the windows in the house in the picture?",
"answers": [
    "white",
    "yellow",
    "blue"
],
"category": "part1 -> basic_recognition -> major"
```
The "img_path" indicates the path to the image in *imgs.zip*, the "question" is a string, the "answers" is a list of answer candidates (several false answers and the correct answer).

The correct answers are kept confidential to ensure A-Bench retains its long-term value as a benchmark for assessing AIGI evaluation capabilities.

###  Test without API
To test with your LMM, we suggest using the following prompt:

```python
import json
with open("Abench.json", "r") as f:
    f = f.read()
    data = json.loads(f)

for item in data:
    image_file = 'path-to-imgs' + item["img_path"]
    message = item["question"] + "\n"
    for choice, ans in zip(["A.", "B.", "C.", "D."], item["answers"]):
        message += f"{choice} {ans}\n"
    message = message + "Answer with the option's letter from the given choices directly."
    print(message)

    # What is the color of the windows in the house in the picture?
    # A.white
    # B.yellow
    # C.blue
    # Answer with the option's letter from the given choices directly.

    # do your test here
    # response = LMM(image_file,message)
    item['response'] = response
    with open("results.jsonl", "a") as wf:
            json.dump(item, wf)
            wf.write("\n")
```

After finishing validation, you can submit the results via [e-mail](zzc1998@sjtu.edu.cn) to get your LMM results on A-Bench !

## Contact

Please contact any of the first authors of this paper for queries.

- Zicheng Zhang, `zzc1998@sjtu.edu.cn`, @zzc-1998
- Haoning Wu, `haoning001@e.ntu.edu.sg`, @teowu

## Citation

If you find our work interesting, please feel free to cite our paper:

```bibtex
@misc{zhang2024abench,
      title={A-Bench: Are LMMs Masters at Evaluating AI-generated Images?}, 
      author={Zicheng Zhang and Haoning Wu and Chunyi Li and Yingjie Zhou and Wei Sun and Xiongkuo Min and Zijian Chen and Xiaohong Liu and Weisi Lin and Guangtao Zhai},
      year={2024},
      eprint={2406.03070},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
