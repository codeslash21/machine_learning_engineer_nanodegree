# Machine Learning Cloud Platforms:

## Amazon Web Services (AWS):
Amazon Web Services (AWS) SageMaker is Amazon's cloud service that allows you to build, train, and deploy machine learning models. Some advantages to using Amazon's SageMaker service are the following:

  - Flexibility in Machine Learning Software: SageMaker has the flexibility to enable the use of any programming language or software framework for building, training, and deploying machine learning models in AWS. For the details see the three methods of modeling within SageMaker below.
    - Built-in Algorithms - There are at least fifteen built-in algorithms that are easily used within SageMaker. Specifically, built-in algorithms for discrete classification or quantitative analysis using linear learner or XGBoost, item recommendations using factorization machine, grouping based upon attributes using K-Means, an algorithm for image classification, and many other algorithms.
    - Custom Algorithms - There are different programming languages and software frameworks that can be used to develop custom algorithms which include: PyTorch, TensorFlow, Apache MXNet, Apache Spark, and Chainer.
    - Your Own Algorithms - Regardless of the programming language or software framework, you can use your own algorithm when it isn't included within the built-in or custom algorithms above.
  - Ability to Explore and Process Data within SageMaker: SageMaker enables the use of Jupyter Notebooks to explore and process data, along with creation, training, validation, testing, and deployment of machine learning models. This notebook interface makes data exploration and documentation easier.
  - Flexibility in Modeling and Deployment: SageMaker provides a number of features and automated tools that make modeling and deployment easier. For the details on these features within SageMaker see below.
    - Automatic Model Tuning: SageMaker provides a feature that allows hyperparameter tuning to find the best version of the model for built-in and custom algorithms. For built-in algorithms SageMaker also provides evaluation metrics to evaluate the performance of your models.
    - Monitoring Models: SageMaker provides features that allow you to monitor your deployed models. Additionally with model deployment, one can choose how much traffic to route to each deployed model (model variant). More information on routing traffic to model variants can be found here and here .
    - Type of Predictions: SageMaker by default allows for On-demand type of predictions where each prediction request can contain one to many requests. SageMaker also allows for Batch predictions, and request data size limits are based upon S3 object size limits. 
