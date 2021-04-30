# Title generation from abstracts 
In this project we try to build a model that can generate a suitable title given an abstract of a technical paper.<br>
We use the following two approaches :-
<br>1. <b>Baseline model</b> - A simple lstm based seq2seq model. Code for this model is present in the folder named <i>baselines</i>.
<br>2. <b>Final model</b> - Implemented title generation based on multi-sentence summarization method. Approach taken from the paper - https://www.ijcai.org/Proceedings/2017/0574.pdf. Code for this model is present in the folder <i>final_model</i>.



## Dataset
We use the dataset from kaggle. Link - https://www.kaggle.com/neelshah18/arxivdataset. An extra column "Id" was added in the dataset which was used later for randomly picking some abstracts. The name of this file is <i>data_id.csv</i> and is present in the data folder. Further 1000 random abstracts were selected and stored as <i>data/test_data.csv</i>.

## Result
We conducted five experiements and generated titles for each experiment can be found in the generated_titles folder. For example:- <i>generated_titles/generated_titles_5.csv</i> means the titles generated using the model from experiment 5. 
## Examples
<br> Final model selected was that from experiment 5. Here are few result of generated titles and comparision with baseline :-
<br><b>Abstract 1</b>
<br><i>Recent studies have highlighted the vulnerability of deep neural networks\n(DNNs) to adversarial examples - a visually indistinguishable adversarial image\ncan easily be crafted to cause a well-trained model to misclassify. Existing\nmethods for crafting adversarial examples are based on and \ndistortion metrics. However, despite the fact that distortion accounts\nfor the total variation and encourages sparsity in the perturbation, little has\nbeen developed for crafting -based adversarial examples. In this paper, we\nformulate the process of attacking DNNs via adversarial examples as an\nelastic-net regularized optimization problem. Our elastic-net attacks to DNNs\n(EAD) feature -oriented adversarial examples and include the\nstate-of-the-art attack as a special case. Experimental results on MNIST,\nCIFAR10 and ImageNet show that EAD can yield a distinct set of adversarial\nexamples with small distortion and attains similar attack perfor...</i>
<br><b>Actual Title </b> : EAD: Elastic-Net Attacks to Deep Neural Networks via Adversarial\n Examples
</b>
<br><b>Generated Title(Baseline)</b>
: a new approach to work <unk> of speed up dnns in
<br><b>Generated Title(Final)</b>
: elastic net attacks to adversarial deep neural networks
<br>
<br><b>Abstract 2</b>
<br><i>We analyze differences between two information-theoretically motivated\napproaches to statistical inference and model selection: the Minimum\nDescription Length (MDL) principle, and the Minimum Message Length (MML)\nprinciple. Based on this analysis, we present two revised versions of MML: a\npointwise estimator which gives the MML-optimal single parameter model, and a\nvolumewise estimator which gives the MML-optimal region in the parameter space.\nOur empirical results suggest that with small data sets, the MDL approach\nyields more accurate predictions than the MML estimators. The empirical results\nalso demonstrate that the revised MML estimators introduced here perform better\nthan the original MML estimator suggested by Wallace and Freeman.
</i>
<br><b>Actual Title </b> : Minimum Encoding Approaches for Predictive Modeling
<br><b>Generated Title(Baseline)</b>
: a filters of work <unk> algorithm for work <unk> of
<br><b>Generated Title(Final)</b>
: encoding approaches for predictive analysis    
<br>
<br><b>Abstract 3</b>
<br><i>Neural sequence-to-sequence models have provided a viable new approach for\nabstractive text summarization (meaning they are not restricted to simply\nselecting and rearranging passages from the original text). However, these\nmodels have two shortcomings: they are liable to reproduce factual details\ninaccurately, and they tend to repeat themselves. In this work we propose a\nnovel architecture that augments the standard sequence-to-sequence attentional\nmodel in two orthogonal ways. First, we use a hybrid pointer-generator network\nthat can copy words from the source text via pointing, which aids accurate\nreproduction of information, while retaining the ability to produce novel words\nthrough the generator. Second, we use coverage to keep track of what has been\nsummarized, which discourages repetition. We apply our model to the CNN / Daily\nMail summarization task, outperforming the current abstractive state-of-the-art\nby at least 2 ROUGE points.
</i>
<br><b>Actual Title </b> : Get To The Point: Summarization with Pointer-Generator Networks
<br><b>Generated Title(Baseline)</b>
: a new framework for work single linkage learning of deep neural 
<br><b>Generated Title(Final)</b>
: abstractive summarization with pointer generator networks  
<br><i> For more examples see the notebook. Thank you!</i>