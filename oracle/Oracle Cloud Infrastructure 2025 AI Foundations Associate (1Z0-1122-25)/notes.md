# Oracle Data AI Foundation (2025)

## Neural Network Architectures

### Recurrent Neural Networks
- Processes data sequentially and stores hidden states

### Long Short-Term Memory
- Processes data sequentially and can retain the context better through use of gates

### Transformers
- Processes data in parallel
- Uses concept of self attention to better understand the context

## AI Model Categories

### Audio and Speech AI Models
- Recurrent Neural Networks
- Long Short-Term Memory
- Transformers
- Variation Autoencoders
- Waveform Models
- Siamese Networks

### Vision AI Models
- Convolutional Neural Networks
- YOLO
- Generative Adversarial Networks

## Machine Learning Fundamentals

### ML vs DL
- **ML**: Algorithms learn from past data to identify trends and predict outcomes on new data
- **DL**: Algorithms learn from complex data using neural networks and predict outcomes or generate new data

### Learning Types
**Supervised Learning**: Extracting rules from data
**Unsupervised Learning**: Clustering

### Deep Learning
- NN with multiple layers → learn and extract complex features and rules from data

### Neural Networks
- Made up of interconnected nodes or neurons in a layered structure that resembles the human brain
- Function approximation is a technique for estimating an unknown underlying function using historical observations from the domain

### ML Categories
- **Supervised**: Classify data or make predictions
- **Unsupervised**: Understand relationships within data sets
- **Reinforcement**: Make decisions or choices

## ML Examples

### Supervised
- Disease detection
- Weather forecasting
- Stock price prediction
- Spam detection
- Credit scoring

### Unsupervised
- Fraudulent transactions detection
- Customer segmentation
- Outlier detection
- Targeted marketing campaigns

### Reinforcement
- Automated robots
- Autonomous cars
- Video games

## When ML is NOT Optimal

- **Simpler Alternatives**: Rule-based approach used for sorting, validating, and verification
- **Insufficient Data**: Self driving cars data set is not extensive enough to handle adverse situations
- **High Costs**: Basic image and text processing ML resizing, filtering, counting
- **Complex Data Handling**: Feature extraction from unstructured data
- **Scalability**: Scaling to large data sets and complex problems

## Classification

- A Supervised ML technique used to categorize or assign data points into predefined classes based on their features or attributes
- **Example**: Logistic regression

### Logistic Regression
- Predicts the output of a categorical dependent variable, given a set of independent variables
- Gives the output in the form of probabilities between 0 and 1
- Uses a sigmoidal function that helps in modelling Binary Classification problems

### Evaluation Metrics for Classification (categorical)
- **Accuracy**: Ratio of correct predictions to the total number of predictions
- **Precision**: Ratio of true positive cases to all positive cases
- **Recall**: Proportion of actual positives which was identified correctly

## Supervised Machine Learning Steps

1. Data Access
2. Data Preparation
3. Modeling
4. Validation
5. Deployment
6. Monitoring and Iteration

## Regression (continuous)

- A Supervised Machine Learning technique used to predict continuous values based on input data
- Linear regression is the simplest form of regression

### Linear Regression Model for Weight Prediction
- Used to find the straight line or hyperplane that best fits a set of points
- **Regression Line**: We fit the simple line model, which passes through most of the data points

### Loss: Train a Model
- Loss is a number indicating how far the predicted value is from the actual value
- **Train a Model**: Determining optimal values for all the weights and bias from labeled examples, so that the loss is minimized

### Evaluation Metrics for Regression
- The correctness of the linear model can be evaluated by different evaluation metrics
- Evaluation metrics are computed using the unseen data
- Mean Absolute Error
- Mean Squared Error (MSE)
- R-Squared

## Unsupervised Learning

- Unlabelled, algorithms learns the patterns of similar group: clustering
- **Examples**: Market segmentation, outlier analysis, recommendation system

### Workflow
1. Prepare data: remove missing values, normalize the data, perform feature scaling
2. Create similarity metrics: choose a similarity metric based on nature of data and clustering algorithms
3. Run clustering algo: use the chosen similarity metrics to cluster the data
4. Interpret results and adjust clustering: check the quality of your clustering output by verifying against expectations iteratively

### Types of Clustering Algorithms
- **Partition-Based**: K-Means
- **Hierarchical-Based**: Dendograms
- **Density-Based**: DBSCAN
- **Distribution-Based**: Gaussian Mixture Model

### K-means Process
1. Initialization
2. Assign Data Points
3. Update Centroids

## Deep Learning = ANN

### ANN Components
- **Layers**: Input, hidden, and output layers receive inputs, transform it, and produce output
- **Neurons**: Computational unit from an input and produces an output
- **Weights**: Determines the strength of connection between neurons
- **Activation Function**: Works on the weighted sum of inputs to a neuron and produces an output
- **Bias**: Additional input to a neuron that allows certain degree of flexibility

### Training Process
- Guess and compare → measure error → adjust guess → update weights

## Sequence Models

- Input data is in the form of sequences
- The goal is to find patterns and make predictions

### Recurrent Neural Network (RNN)
- Handles sequential data
- Maintains a hidden state or memory
- Allows information to persist using a feedback loop
- Captures dependencies

### Long Short-Term Memory (LSTM)
- Works by using a specialized memory cell and gating mechanisms to capture long-term dependencies in sequential data
- Selectively remembers or forgets information over time

#### LSTM Components
- Input Processing
- Previous Memory
- Gating Mechanism
  - Input gate
  - Forget gate
  - Output gate
- Updating Memory: Updates the cell state by using the information of input gate and forget gate
- Output Generation: Generates the output of LSTM for current time step

## Convolutional Neural Networks (CNN)

### Layers
- Input layer
- Feature extractions layer
- Classification layers

### Feature Extraction Layers
- **Convolution layer**: Applies convolutional operations to the input image using small filters known as kernels
- **Activation layer**: Allows the network to learn more complex and nonlinear relationships in the data
- **Pooling layer**: Helps reduce computational complexity and also the spatial dimensions of the feature maps generated by the convolutional layers

### Limitations of CNN
- **Computation**: Requires massive data and computations
- **Overfitting**: Happens with limited training data
- **Interpretability**: Typical Black Box models
- **Sensitivity**: Highly sensitive to input variations

## Language Models

- **LM**: a probabilistic model of text
- **LLM**: Large parameters

## RNN vs Transformers

### RNN (sequence)
- Sequential data, maintains hidden state or memory, captures dependencies, allows information to persist using a feedback loop
- **Issues**: Struggle with Long-Range Dependencies

### Transformer
- Understand relationships between all words in a sentences
- **Attention Mechanism**: Add context to the text
- **Encoder-Decoder** architecture

#### Encoder
- Read input text, embedding, use attention mechanism

#### Decoder
- Generate output from embeddings
- **Tokens** rather than words for computer
- **Embeddings**: numerical representations for text → number sequences (vectors)

### Transformer Model Types

#### Encoder only
- Transforms input data into a sequence of vectors
- Useful for understanding input data without generating a new sequence
- **Example**: Semantic Search

#### Decoder only
- Generate sequences, such as text, based on a given input
- Useful for tasks that involve generating data
- **Example**: Text Generation

#### Encoder-Decoder
- Combines an encoder for input processing and a decoder for sequence generation
- Useful for sequence-to-sequence tasks
- **Example**: Machine Translation

## Prompt Engineering

### Prompt
- The input or initial text provided to the model

### Prompt Engineering
- The process of iteratively refining a prompt for the purpose of eliciting a particular style of response

### In-context Learning
- Conditioning (prompting) an LLM with instructions and or demonstrations of the task it is meant to complete
- **k-shot prompting**: explicitly providing k examples of the intended task in the prompt

### Chains-of-Thought Prompting
- Provide examples in a prompt to show responses that include a reasoning step
- Cal logic

## LLM Challenges & Solutions

### Hallucination
- Model generate text that is non-factual ungrounded

### Solutions
- **More context** → RAG Retrieval-Augmented Generation
- **More instruction following** → fine tuning using pretrained model

## Customize LLMs with Your Data

1. Start with a simple Prompt
2. Add Few shot Prompting
3. Add simple retrieval using RAG
4. Fine-tune the model
5. Optimize the retrieval on fine-tuned model

## Oracle ML Services

- Data Science
- ML in Database
- Data Labeling

## Ways to Access Oracle Cloud Infrastructure AI Services

- **OCI Console**: Provides easy-to-use browser-based interface; enables access to notebook sessions and all service features
- **Rest API**: Provides access to service functionality; requires programming expertise
- **Language SDKs**: Provides programming language SDKs for Java, Python, Net, Go, Ruby, and TypeScript/JavaScript
- **CLI**: Provides quick access and full functionality without the need for scripting

## Core Principles of OCI Data Science

- **Accelerated**: Allow data scientists to work how they want, and provide access to automated workflows, the best of open-source libraries, and a streamlined approach to building models
- **Collaborative**: Enable data science teams to work together with ways to share and reproduce models in a structured, secure way for enterprise-grade results
- **Enterprise-Grade**: Provide a fully managed platform, built to meet the needs of the modern enterprise

## Trustworthy AI

1. Follow laws
2. Ethical
3. Robust

## OCI Generative AI Services

- Fully managed service that provides a set of customizable Large Language Models (LLMs) available via a single API to build generative AI applications
- **Choice of Models**: high performing pretrained foundational models from Meta and Cohere
- **Flexible Fine-tuning**: create custom models by fine-tuning foundational models with your own data set
- **Dedicated AI Clusters**: GPU based compute resources that host your fine-tuning and inference workloads

## AI Vector Search Oracle Database 23ai

- SQL support for vector generation
- Vector Data Type
- Similarity search with SQL syntax and functions
- Approximate search indexes

## Select AI

- ChatGPT of Oracle
- Translate human language to oracle SQL language (use SELECT ai, then question)

## OCI Language Services

- 600 categories

## Oracle Speech

- Supported languages: English, Spanish, Portuguese

## Oracle Vision

- Image and document processing
