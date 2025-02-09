[![GitHub license](https://img.shields.io/github/license/SINGHxTUSHAR/IMDB-Analysis.svg)](https://github.com/SINGHxTUSHAR/IMDB-Analysis/blob/master/LICENSE)
[![GitHub contributors](https://img.shields.io/github/contributors/SINGHxTUSHAR/IMDB-Analysis.svg)](https://GitHub.com/SINGHxTUSHAR/IMDB-Analysis/graphs/contributors/)
[![GitHub issues](https://img.shields.io/github/issues/SINGHxTUSHAR/IMDB-Analysis.svg)](https://GitHub.com/SINGHxTUSHAR/IMDB-Analysis/issues/)
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/SINGHxTUSHAR/IMDB-Analysis.svg)](https://GitHub.com/SINGHxTUSHAR/IMDB-Analysis/pulls/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)


[![GitHub watchers](https://img.shields.io/github/watchers/SINGHxTUSHAR/IMDB-Analysis.svg?style=social&label=Watch&maxAge=2592000)](https://GitHub.com/SINGHxTUSHAR/IMDB-Analysis/watchers/)
[![GitHub forks](https://img.shields.io/github/forks/SINGHxTUSHAR/IMDB-Analysis.svg?style=social&label=Fork&maxAge=2592000)](https://GitHub.com/SINGHxTUSHAR/IMDB-Analysis/network/)
[![GitHub stars](https://img.shields.io/github/stars/SINGHxTUSHAR/IMDB-Analysis.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/SINGHxTUSHAR/IMDB-Analysis/stargazers/)

[![Open in Visual Studio Code](https://img.shields.io/static/v1?logo=visualstudiocode&label=&message=Open%20in%20Visual%20Studio%20Code&labelColor=2c2c32&color=007acc&logoColor=007acc)](https://open.vscode.dev/SINGHxTUSHAR/IMDB-Analysis)


# IMDB-Analysis

![preview Image](https://github.com/SINGHxTUSHAR/IMDB-Analysis/blob/6640b0dd684a74116256dcf940602a660f32de8b/preview.png)


#### Project Overview:
Sentiment analysis on the IMDB dataset is a popular Natural Language Processing (NLP) task where the goal is to classify movie reviews as positive or negative. In this analysis, we use a Simple Recurrent Neural Network (RNN) with Embedding layers to capture the sequential nature of text and determine sentiment.

Let me explain how this sentiment analysis system works:

* `Data Preparation`: We use the IMDB dataset, which contains 50,000 movie reviews labeled as positive or negative
Each review is preprocessed into sequences of word indices
We limit our vocabulary to the top 10,000 most frequent words to manage complexity
Reviews are padded to a fixed length of 500 words to ensure uniform input size


* `Embedding Layer`: The first layer is an Embedding layer that converts word indices into dense vectors
Each word is mapped to a 32-dimensional vector space
This allows the model to learn semantic relationships between words
Similar words end up closer together in this embedding space


* `Simple RNN Layer`: The SimpleRNN layer processes the sequence of word embeddings
It maintains a hidden state that captures information about previous words
At each time step, it combines the current input with its previous hidden state
This allows the model to understand context and word relationships
We use 32 units in the RNN layer to capture different aspects of the sequence


* `Output Layer`: A Dense layer with sigmoid activation produces the final prediction output is a single number between 0 and 1Values closer to 1 indicate positive sentiment values closer to 0 indicate negative sentiment


* `Training Process`: The model is trained using binary cross-entropy loss
Adam optimizer is used for efficient training
Training happens in batches of 32 reviews
The model trains for 5 epochs (complete passes through the dataset)
Validation data helps monitor for overfitting


This model typically achieves an accuracy of around 85% on the test set, which is quite good for a simple RNN architecture. However, there are some limitations:

Simple RNNs can struggle with long-term dependencies due to the vanishing gradient problem
The fixed sequence length might truncate longer reviews
The limited vocabulary might miss some important but rare words.



## Requirements💻 :

Ensure you have the following dependencies installed:

- Python (version 3.11.x || 3.12.x)
- IDE: VS-CODE or collab
- Virtual-environment(venv)
- Other dependencies (refer to the requirement.txt)

You can install the required Python packages using:

```bash
pip install -r requirement.txt
```


## Setup 💿:

- Clone the repository:
```bash
git clone https://github.com/SINGHxTUSHAR/NextWordAI.git
cd NextWordAI
```
- Create a virtual environment (optional but recommended):
```bash
python -m venv venv
```
- Activate the virtual environment:
  - On Windows:
   ```bash
   venv\Scripts\activate
   ```
  - On macOS/Linux:
  ```bash
  source venv/bin/activate
  ```


## Contributing 📌:
If you'd like to contribute to this project, please follow the standard GitHub fork and pull request process. Contributions, issues, and feature requests are welcome!

## Suggestion 🚀: 
If you have any suggestions for me related to this project, feel free to contact me at tusharsinghrawat.delhi@gmail.com or <a href="https://www.linkedin.com/in/singhxtushar/">LinkedIn</a>.

## License 📝:
This project is licensed under the <a href="https://github.com/SINGHxTUSHAR/IMDB-Analysis/blob/main/LICENSE">MIT License</a> - see the LICENSE file for details.




