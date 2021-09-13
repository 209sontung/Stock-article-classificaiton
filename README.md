# Stock article title sentiment-based classification using PhoBERT
## <a name="introduction"></a> Introduction
Text classification is a typical and important part of supervised learning, it has several applications in economics and attracted the attention of many stock market investors. For a long time, the news is frequently an unanticipated stock investment variable that instantaneously influences stock price directions.  In front of an enormous volume of news, investors are always searching for models that automatically categorize news quickly and accurately. Thus, we have utilized [PhoBERT](https://github.com/VinAIResearch/PhoBERT) to classify news articles into three categories [negative,  neutral,  or positive] based on their titles. The results demonstrated that after training with a dataset of over 1000  news samples from CafeF.vn, our model achiveved an accuracy up to 93% in the classification task.
## <a name="start"></a> Getting Started
### Installation
```python
!pip install transformers
!pip install fastBPE
!pip install fairseq

# Install the vncorenlp python wrapper
!pip install vncorenlp

# Download VnCoreNLP-1.1.1.jar & its word segmentation component (i.e. RDRSegmenter) 
!mkdir -p vncorenlp/models/wordsegmenter
!wget https://raw.githubusercontent.com/vncorenlp/VnCoreNLP/master/VnCoreNLP-1.1.1.jar
!wget https://raw.githubusercontent.com/vncorenlp/VnCoreNLP/master/models/wordsegmenter/vi-vocab
!wget https://raw.githubusercontent.com/vncorenlp/VnCoreNLP/master/models/wordsegmenter/wordsegmenter.rdr
!mv VnCoreNLP-1.1.1.jar vncorenlp/ 
!mv vi-vocab vncorenlp/models/wordsegmenter/
!mv wordsegmenter.rdr vncorenlp/models/wordsegmenter/
```
