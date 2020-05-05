
# Deployment of Machine Learning Models:
There are three primary components of deployments. These are -
  > * Explore and process data.</br>
  > * Modeling or model your data.</br>
  > * Deployment or deploy your model.
  
  </br>
<img src="../Images/ml-concepts-10.png", width="500"/>

* **Cloud Computing:** Cloud computing can simply be thought of as transforming an Information Technology (IT) product into a service. With our vacation photos example, we transformed storing photos on an IT product, the flash drive; into storing them using a service, like Google Drive. Using a cloud storage service provides the benefits of making it easier to access and share your vacation photos, because you no longer need the flash drive. 
  * **Why would a business decide to use cloud computing?** Most of the factors related to choosing cloud computing services, instead of developing on-premise IT resources are related to time and cost. The capacity utilization graph below shows how cloud computing compares to traditional infrastructure (on-premise IT resources) in meeting customer demand.
  
</br>
<img src="../Images/capacityutilizationcurve3.png", width="500"/>
  
  * **Benefits of Risks Associated with Cloud Computing:**
  
    * **Benifits:** </br>
      **1.** Reduced Investments and Proportional Costs (providing cost reduction).</br>
      **2.** Increased Scalability (providing simplified capacity planning).</br>
      **3.** Increased Availability and Reliability (providing organizational agility).</br>
      
    * **Risks:** </br>
      **1.** (Potential) Increase in Security Vulnerabilities.</br>
      **2.** Reduced Operational Governance Control (over cloud resources).</br>
      **3.** Limited Portability Between Cloud Providers.</br>
      **4.** Multi-regional Compliance and Legal Issues.</br>
      
### Paths to Deployment:
Followings are the three steps to deploy a model using Amazon's Sagemaker -
  - **Python model is recoded into the programming language of the production environment:** The first method which involves recoding the Python model into the language of the production environment, often Java or C++. This method is rarely used anymore because it takes time to recode, test, and validate the model that provides the same predictions as the original.
  - **Model is coded in Predictive Model Markup Language (PMML) or Portable Format Analytics (PFA):** The second method is to code the model in Predictive Model Markup Language (PMML) or Portable Format for Analytics (PFA), which are two complementary standards that simplify moving predictive models to deployment into a production environment. The Data Mining Group developed both PMML and PFA to provide vendor-neutral executable model specifications for certain predictive models used by data mining and machine learning.
  - **Python model is converted into a format that can be used in the production environment:** The third method is to build a Python model and use libraries and methods that convert the model into code that can be used in the production environment. Specifically most popular machine learning software frameworks, like PyTorch, TensorFlow, SciKit-Learn, have methods that will convert Python models into intermediate standard format, like ONNX (Open Neural Network Exchange format). This intermediate standard format then can be converted into the software native to the production environment.
  
  </br>
<img src="../Images/mlworkflow-devops-1.png", width="500"/>




#### NOTE:
  - Cloud Computing can be used for any or all parts of the machine learning process.
  - **Environment** is the computational system that host the application. Types of the environment depends on the types of users. With examples, if we are providing predictions to the users who are customer then its called `production environment`, and if the users are emplyees testing the applicatin it would be the `test environment`.
  - **Endpoint:** Application communicates with the model through an interface to the model called endpoint.
    - Allows the application to send user data to the model and
    - Receives predictions back from the model based upon that user data.
   One way to think of the endpoint that acts as this interface, is to think of a Python program where:
    - the endpoint itself is like a function call
    - the function itself would be the model and
    - the Python program is the application.
    
</br>
  <img src="../Images/endpointprogram-1.png", width="500"/>
  
  
### Endpoint and REST API
Communication between the application and the model is done through the endpoint (interface), where the endpoint is an Application Programming Interface (API).
  - An easy way to think of an API, is as a set of rules that enable programs, here the application and the model, to communicate with each other.
  - In this case, our API uses a REpresentational State Transfer, REST, architecture that provides a framework for the set of rules and constraints that must be adhered to for communication between programs.
  - This REST API is one that uses HTTP requests and responses to enable communication between the application and the model through the endpoint (interface).
  - Noting that both the HTTP request and HTTP response are communications sent between the application and model.

### HTTP Request:
The HTTP request that’s sent from your application to your model is composed of four parts:

  - **Endpoint:**
This endpoint will be in the form of a URL, Uniform Resource Locator, which is commonly known as a web address.
  - **HTTP Method:**
Below you will find four of the HTTP methods, but for purposes of deployment our application will use the POST method only.
  - **HTTP Headers:**
The headers will contain additional information, like the format of the data within the message, that’s passed to the receiving program.
  - **Message (Data or Body):**
The final part is the message (data or body); for deployment will contain the user’s data which is input into the model.

</br>
<img src="../Images/httpmethods.png", width="500"/>

### HTTP Response:
The HTTP response sent from your model to your application is composed of three parts:
  - **HTTP Status Code:**
If the model successfully received and processed the user’s data that was sent in the message, the status code should start with a 2, like 200.
  - **HTTP Headers:**
The headers will contain additional information, like the format of the data within the message, that’s passed to the receiving program.
  - **Message (Data or Body):**
What’s returned as the data within the message is the prediction that’s provided by the model.
</br>
This prediction is then presented to the application user through the application. The endpoint is the interface that enables communication between the application and the model using a REST API.
</br>
As we learn more about RESTful API, realize that it's the application’s responsibility:
  - To format the user’s data in a way that can be easily put into the HTTP request message and used by the model.
  - To translate the predictions from the HTTP response message in a way that’s easy for the application user’s to understand.
