# Computer Vision

## Topic: Detecting Violent Content in Social Media Images 

Social media has become a primary mode of consumption for news and current events. Therefore, having a variety of content without description in the age of information, how can we evaluate content specifically for sensitive and violent images? Is there an algorithm that can estimate violence?

This leads to a paper on Implementation of the model used in the paper **_Protest Activity Detection and Perceived Violence Estimation from Social Media Images_** (ACM Multimedia 2017) [\[arxiv\]](https://arxiv.org/abs/1709.06204) *by Donghyeon Won, Zachary C. Steinert-Threlkeld, Jungseock Joo*.

Utilizing this paper's algorithm we added a GRAD-CAM for more interpretability to identify where the algorithm is picking up the violence estimations.

## Install
1. Clone this repo locally `git clone git@github.com:robbjr99/AIPI540-Module1Project.git`
2. Create virtual environment `python -m venv venv_name`
3. Install the libraries and dependencies `pip install -r requirements.txt`
4. Run main python notebook

## Usage   
#### Training  

```bash
python train.py --data_dir UCLA-protest/ --batch_size 32 --lr 0.002 --print_freq 100 --epochs 100 --cuda
```

#### Evaluation

```bash
python pred.py --img_dir path/to/some/image/directory/ --output_csvpath result.csv --model model_best.pth.tar --cuda
```

## Authors
- Robert Baldoni
- Miranda Morris
- Hearsch Jariwala
