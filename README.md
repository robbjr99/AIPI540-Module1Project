# Computer Vision

## Topic: Detecting Violent Content in Social Media Images 

Social media has become a primary mode of consumption for news and current events. Therefore, having a variety of content without description in the age of information, how can we evaluate content specifically for sensitive and violent images? Is there an algorithm that can estimate violence?

This leads to a paper on Implementation of the model used in the paper **_Protest Activity Detection and Perceived Violence Estimation from Social Media Images_** (ACM Multimedia 2017) [\[arxiv\]](https://arxiv.org/abs/1709.06204) *by Donghyeon Won, Zachary C. Steinert-Threlkeld, Jungseock Joo*.

Utilizing this paper's algorithm we added a GRAD-CAM for more interpretability to identify where the algorithm is picking up the violence estimations. For PowerPoint link click [here](https://github.com/robbjr99/AIPI540-Module1Project/blob/main/CV%20Module%201.pptx).

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

## Results
Gradient-weighted Class Activation Mapping (Grad-CAM), uses the gradients model’s attributes which contribute to the prediction of the level of perceived violence. A localization heat map is produced, highlighting the key regions in the image as identified by the model. More about Grad-CAM can be found [here](https://arxiv.org/abs/1610.02391).


<img width="318" alt="result1" src="https://user-images.githubusercontent.com/88054926/153778084-02451230-680f-4fa7-b23d-7bc9b8a3b07e.png">
<img width="318" alt="result2" src="https://user-images.githubusercontent.com/88054926/153778085-4aa46b0f-3951-46af-8f9b-8e596a363fcf.png">

## Authors
- Robert Baldoni
- Miranda Morris
- Hearsch Jariwala
