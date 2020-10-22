# University of Washington | DATA 512 - Human Centered Data Science

## Assignment 2: Bias in Data

-------------------------------------------------------------------------------

Have you ever wonder what is the distribution of toxicity score be?
![](Resource/A2_chart_toxicity_score-kernel_density.jpg)  

How about the distribution of aggression score?
![](Resource/A2_chart_aggression_score-kernel-density.jpg)


Hope these two visualizations caught your desire to know more about this topic. In this project, we will analyze and will have a better understanding about these two areas.

## Summary
The objective of this assignment is to examine the potential sources of bias in a corpus of human-annotated data (Wikipedia Talk Corpus) and describe some implications of those biases in connecting to [Perspective API](https://github.com/conversationai/perspectiveapi/wiki/perspective-hacks)


## Data Source
The data we use in this assignment is "Wikipedia Talk Labels" which you can download from this [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731)

There are three separate datasets. You can download these datasets from the Figshare website and store on your project working directory.

1. Toxicity
  * 160k labeled comments from English Wikipedia by approximately 10 annotators via Crowdflower on a spectrum of how toxic the comment is (perceived as likely to make people   want to leave the discussion) to how healthy to conversation the contribution is.
  * Link to [Toxicity](https://github.com/ewulczyn/wiki-detox/blob/master/src/modeling/toxicity_question.png) questionaire

2. Aggression
  * 100k labeled comments from English Wikipedia by approximately 10 annotators via Crowdflower on how aggressive the comment was perceived to be. We also include some demographic data for each crowd-worker.
  * Link to [Aggression](https://github.com/ewulczyn/wiki-detox/blob/master/src/modeling/aggression_question.png) questionaire

3. Personal Attacks
  * 100k labeled comments from English Wikipedia by approximately of 10 annotators via Crowdflower on whether it contains a personal attack. We also include some demographic data for each crowd-worker.
  * Link to [Personal Attack](https://github.com/ewulczyn/wiki-detox/blob/master/src/modeling/attack_question.png) questionaire


## Data Description
An overview of the data is available [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release)
* These datasets are released under a CC0 public domain dedication by the source.
* These datasets can also be cited as: Citation: Wulczyn, Ellery; Thain, Nithum; Dixon, Lucas (2016): Wikipedia Detox. figshare. doi.org/10.6084/m9.figshare.4054689

Each individual dataset contains three separate TSV files: annotations, annotated comments, and worker demographics. Each dataset contains thousands of online discussion posts made by Wikipedia editors. Crowdworkers labelled these posts for three kinds of histile speech: toxicity, aggression, and personal attacks

![](Resource/data_1_pic.JPG)

![](Resource/data_2_pic.JPG)

![](Resource/data_3_pic.JPG)

![](Resource/data_4_pic.JPG)

![](Resource/data_5_pic.JPG)


## Motivation for the analysis
Social bias online has been gaining steam in the last five years. The more interaction users perform online, the larger data it produces with comments include toxicity and aggression. Therefore, i am interested in knowing more about the bias in these two areas: toxicity and aggression.

There are two hypothesis/questions that i want to find out:

1. Is there a bias relationships between worker demographics and labeling behavior in toxicity?
2. Is there a bias relationships between worker demographics and labeling behavior in aggression?

## Code structure
All of the analysis and the detail step by step are in one Jupyter notebook file which you can find from this GitHub repository.
The images of visualization charts are also available in this repository inside the Resource folder.

## Helpful Notes
As you follow along the analysis from this repository as well as the Jupyter Notebook, there are some helpful tips i want to share to ensure you reproduce the analysis with no issue.
1. The datasets i chose to analyze are Toxicity and Aggression. Each dataset has three separate TSV files. You wonder why i dont have the data files on this GitHub repository. These raw data files are huge (more than 25 MB in size most of the time), GitHub won't allow to upload them on the repository so i couldn't load them here. However, i have include a direct link to [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731) in this README file, that way you can always grab the latest data files directly from the main source.

2. For the Exploratory Data Analysis (EDA), it is a process to explore the data in a logical approach. The next steps depend on the previous steps to ensure we reach the final outcome. The Jupyter Notebook has the detail of steps that you can follow along in sequence for the EDA.

3. I add my comments along the way for major points throughout the EDA, these will be helpful to provide the context and logical thinking about the results from the EDA at that particular stage.

4. In my final results on the Jupyter Notebook, i discuss the outcome for each analysis: 
* What did i found?
* Did i find bias? 
* What i did not?

I documented my judgement about not doing the analysis for raw text from the comments. Some of the comments (i.e. explicit words) are not approriate to display from the result nor the visualization as well as online GitHub community. In the spirit of privacy and ethical research principle, it is better to skip the analysis for this raw comment text. I believe, we already have enough analysis to identify the bias from this study. 

