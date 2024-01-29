<h1>Bank Marketing - Term Deposit Prediction with Trees and Explainable AI (XAI)</h1>
<img src="https://github.com/JiaHui-TANG/Bank-Marketing---Term-Deposit-Prediction-with-Trees-and-Explainable-AI/blob/610fa7baf80ac255874cfdb70804a51b913ba33e/bank-term-deposit-tree-xai.png" style="width:800px;height:450px;">

<h2>Description</h2>
<p>Term deposit is a fixed-term investment that includes the deposit of money into an account at a financial institution. It carries short-term maturities ranging from 1 month to a few years and will have varying levels of required minimum deposits. The bank uses the money or these funds for lending to other consumers/businesses and in return pays the depositor compensation in interest on the term deposit account.</p>
<p>While banks adopted numerous marketing techniques to sell term deposits to their customers such as email marketing, advertisements, telephonic marketing, and digital marketing, telephonic marketing campaigns remained as one of the most effective ways to reach out to people. However, it involves heavy investment in large call centers and staff training to execute these campaigns which can be costly and time-consuming.</p>

<h2>Project Objective</h2>
<p>To target the term deposit marketing to individuals who are likely to engage with the bank's term deposit, focusing their marketing effort on this group of potential customers and contributing to boosting the marketing team's efficiency and ROI.</p>

<h2>Data Source</h2>
<p>The data is about direct marketing campaigns (phone calls) from a Portuguese banking institution that aims to predict if a client will subscribe to a term deposit. Often more than 1 phone call to the same client was required to access if the client would or wouldn't subscribe to the bank's term deposit.</p>
<table>
    <strong>Table 1: Data Dictionary - Features and their definition</strong>
    <tr>
        <th>Feature Name</th>
        <th>Definition</th>
        <th>Key</th>
    </tr>
    <tr>
        <td>Age (Numeric)</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Job (Categorical)</td>
        <td>Type of Job / Job status</td>
        <td>Key: {"admin","unknown","unemployed","management","housemaid","entrepreneur","student", "blue-collar","self-employed","retired","technician","services"}</td>
    </tr>
    <tr>
        <td>Marital (Categorical)</td>
        <td>Client's Marital Status</td>
        <td>Key: {"married","divorced","single"}
        <br> Note: divorced means divorced or widowed
        </td>
    </tr>
    <tr>
        <td>Education (Categorical)</td>
        <td>Highest Education Level Obtained</td>
        <td>Key: {"unknown","secondary","primary","tertiary"}</td>
    </tr>
    <tr>
        <td>Default (Binary)</td>
        <td>Has credit in default</td>
        <td>Key: {"yes", "no"}</td>
    </tr>
    <tr>
        <td>Balance (Numeric)</td>
        <td>Average yearly balance (euros)</td>
        <td></td>
    </tr>
    <tr>
        <td>Housing (Binary)</td>
        <td>A person has housing loan</td>
        <td>Key: {"yes", "no"}</td>
    </tr>
    <tr>
        <td>Loan (Binary)</td>
        <td>A person has personal loan</td>
        <td>Key: {"yes", "no"}</td>
    </tr>
    <tr>
        <td>Contact (Categorical)</td>
        <td>TD related contact communication type</td>
        <td>Key: {"unknown", "cellular", "telephone"}</td>
    </tr>
    <tr>
        <td>Day (Numeric)</td>
        <td>Last contact day of the month</td>
        <td>Key: {1-31}</td>
    </tr>
    <tr>
        <td>Month (Categorical)</td>
        <td>Last contact month of year</td>
        <td>Key: {"jan", "feb", "mar", ..., "nov", "dec}</td>
    </tr>
    <tr>
        <td>Duration (Numeric)</td>
        <td>Last contact duration in seconds</td>
        <td></td>
    </tr>
    <tr>
        <td>Campaign (Numeric, Inclusive of last contact)</td>
        <td>Number of contacts performed during this campaign and for this client</td>
        <td></td>
    </tr>
    <tr>
        <td>pdays (Numeric)</td>
        <td>Number of days passed by after the client was last contacted from a previous campaign</td>
        <td>Note: -1 means client was not previously contacted</td>
    </tr>
    <tr>
        <td>previous (Numeric)</td>
        <td>Number of contacts performed before this campaign and for this client</td>
        <td></td>
    </tr>
    <tr>
        <td>poutcome (Categorical)</td>
        <td>Outcome of previous marketing campaign</td>
        <td>Key: {"unknown", "other", "failure", "success"}</td>
    </tr>
    <tr>
        <td>y - Desired Target (Binary)</td>
        <td>Client has subscribed to a term deposit</td>
        <td>Key: {"yes", "no"}</td>
    </tr>
</table>
      
<h2>Python Packages Used</h2>
<ul>
  <li>Python 3.10.0</li>
  <li>klib 1.1.2</li>
  <li>shap 0.44.1</li>
  <li>tensorflow_decision_forests 1.8.1</li>
  <li>wurlitzer 3.0.3</li>
  <li>catboost 1.2.2</li>
  <li>dtreeviz 2.2.2</li>
  <li>gradio 4.12.0</li>
</ul>

<h2>Approaches</h2>
<ol>
  <li>Data Acquisition: Import data with API call</li>
  <li>Data validation and Exploratory Data Analysis with Plotly and klib</li>
  <li>Developed Random Forest (TF), Gradient Boosted Trees (TF), XGBoost, Catboost, LightGBM and saving weights for model serving</li>
  <li>Plot the above models' interpretations and feature importance according to Shap values with Shapely</li>
</ol>
<h2>Deployment and Demonstration</h2>
<a href=https://huggingface.co/spaces/jia-hui-tang/bank-marketing-term-deposit-prediction?logs=container>Click here to use the prediction model!</a>

<h3>Acknowledgements:</h3>
1. Dataset & Brief Domain Knowledge: Banking Marketing
2. Term Deposit Definition: Term Deposit: Definition, How it's used, rates, and how to invest
3. Pros & Cons of Telemarketing: Telemarketing - Advantages and disadvantages of telemarketing
