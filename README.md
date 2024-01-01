# Advance House Price Prediction using Sagemaker

The House Price Predictor is an advanced machine learning application designed to predict house prices based on various features. Utilizing Amazon SageMaker, this project employs powerful algorithms to analyze historical real estate data and provide accurate predictions for property values. The application is user-friendly, making it an invaluable tool for homebuyers, sellers, and real estate professionals seeking data-driven insights. It employs advanced machine learning algorithms, coupled with AWS GuardRail, and Shadow Testing methodologies, for better scalability and consistency of the deployed application. AWS Jumpstart is also used to train the model using Low Code approach.

## Key Components:
1. **Amazon SageMaker Integration:**
Seamlessly integrates with Amazon SageMaker, a fully managed machine learning service, to streamline model training, deployment, and scaling.

2. **AWS Jumpstart for Efficient Model Training:**
Expedites model training through AWS Jumpstart, leveraging pre-configured machine learning environments for rapid development and deployment.

3. **GuardRail for Model Governance:**
Enforces model governance and compliance through GuardRail, ensuring adherence to ethical and regulatory standards.

4. **Shadow Testing for Deployment Confidence:**
Implements Shadow Testing during deployment to run the model alongside the existing system, providing confidence in performance before full-scale deployment.

## AWS Setup:
1. **S3 bucket:** Create 3 buckets for model training, Jumpstart, and GuardRail
    - **Bucket 1:** Contains training dataset
    - **Bucket 2:** Contains pre-processed train, test, and validate dataset. Make sure to rename each csv file as data.csv (Make seperate directories for each).
    - **Bucket 3:** Contains 3 models, and pre-processed test data.
2. **IAM Role:** Create an IAM role that gives read and write permission on the previously created buckets by Sagemaker.
3. **AWS Sagemaker:** Create a notebook for model training and hyperparameter tuning.

## Project Dataset: 
[Kaggle Dataset URL](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)

### Advantages of Using AWS GuardRail:
1. **Model Governance and Compliance:**
   - GuardRail ensures adherence to predefined policies and regulatory standards, promoting ethical and compliant use of machine learning models.

2. **Transparency and Accountability:**
   - By enforcing model governance, GuardRail enhances transparency and accountability in the development and deployment of machine learning models. This is crucial for building trust in the model's predictions.

3. **Risk Mitigation:**
   - GuardRail helps identify and mitigate potential risks associated with the model's behavior, ensuring that the deployed model aligns with ethical considerations and business objectives.

4. **Automated Policy Enforcement:**
   - GuardRail automates the enforcement of governance policies, reducing the likelihood of human error and ensuring consistent adherence to guidelines across different stages of the machine learning lifecycle.

5. **Alerts and Notifications:**
   - The system provides alerts and notifications when there are deviations from established governance policies, allowing for prompt action and resolution.

6. **Scalability and Consistency:**
   - GuardRail scales with the model deployment, providing consistent governance across various deployment scenarios and preventing governance-related challenges as the system expands.

### Advantages of Using Shadow Testing:
1. **Confidence in Model Deployment:**
   - Shadow Testing allows for running the new model alongside the existing system without affecting real user interactions. This provides confidence in the model's performance before it is fully deployed, reducing the risk of unexpected issues.

2. **Realistic Simulation:**
   - By simulating real-world scenarios, Shadow Testing provides a more accurate representation of how the model will behave in a production environment. This includes handling various inputs and interactions that may occur during actual usage.

3. **Early Detection of Issues:**
   - Running the model in parallel with the existing system during Shadow Testing enables the early detection of potential issues or discrepancies between the expected and actual model behavior, allowing for timely adjustments.

4. **Risk Mitigation:**
   - Shadow Testing helps mitigate the risk of deploying a model with unintended consequences by allowing developers to observe its behavior and impact in a controlled setting before it becomes fully operational.

5. **User Experience Assessment:**
   - By observing the model in a shadow environment, developers can assess its impact on user experience, ensuring that the deployment does not negatively affect end-users.

6. **Gradual Rollout:**
   - Shadow Testing facilitates a gradual rollout strategy, where the new model can be introduced incrementally and its performance monitored, ensuring a smooth transition without disrupting the entire system at once.

Both AWS GuardRail and Shadow Testing contribute to the overall robustness, reliability, and ethical deployment of machine learning models, ensuring that they meet regulatory standards, perform as expected, and provide a positive user experience.
