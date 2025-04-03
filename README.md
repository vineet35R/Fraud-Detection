# Fraud-Detection

<H3>Overview</H3>

This repository contains the code and analysis for a fraud detection . The goal was to classify whether a transaction was fraudulent based on transactional and identity data. The dataset consisted of approximately 590,540 training samples (3.5% fraud), 506,691 test samples and with 394 features.

<h3>Dataset</h3>
 <h4>IEEE-CIS Fraud Detection Kaggle Competition Dataset</h4>
    <ul>
        <li><strong>TransactionDT:</strong> Timedelta from a given reference datetime (not an actual timestamp), but the time difference in seconds from a certain time.</li>
        <li><strong>TransactionAMT:</strong> Transaction payment amount in USD, the decimal part is worth paying attention to.</li>
        <li><strong>ProductCD:</strong> Product code, the product for each transaction. It may not necessarily be an actual product but may also refer to a service.</li>
        <li><strong>card1-card6:</strong> Payment card information, such as card type, card category, issue bank, country, etc.</li>
        <li><strong>addr1-addr2:</strong> Address, billing region and billing country.</li>
        <li><strong>dist:</strong> Distances between (not limited) billing address, mailing address, zip code, IP address, phone area, etc.</li>
        <li><strong>P_ and R_ emaildomain:</strong> Purchaser and recipient email domain, some transactions do not require the recipient, and the corresponding Remaildomain is empty.</li>
        <li><strong>C1-C14:</strong> Counting, such as how many addresses are found to be associated with the payment card, etc.</li>
        <li><strong>D1-D15:</strong> Timedelta, such as days between previous transaction, etc.</li>
        <li><strong>M1-M9:</strong> Match, such as names on card and address, etc.</li>
        <li><strong>Vxxx:</strong> Vesta engineered rich features, including ranking, counting, and other entity relations. Some V features are missing in different proportions.</li>
    </ul>

<h3> Model</h3>
 <ul>
        <li>Logistic Regression</li>
        <li>Decision Tree</li>
        <li>Random Forest</li>
        <li>LGBM</li>
        <li>CNN</li>
        <li>LSTM</li>
 </ul>
<h3> Performance</h3>
<table border="1">
    <tr>
        <th>Model</th>
        <th>Public Score (AUC)</th>
        <th>Private Score (AUC)</th>
    </tr>
    <tr>
        <td>Logistic Regression</td>
        <td>0.8461</td>
        <td>0.8477</td>
    </tr>
    <tr>
        <td>Decision Tree</td>
        <td>0.9574</td>
        <td>0.8248</td>
    </tr>
    <tr>
        <td>Random Forest</td>
        <td>0.9999</td>
        <td>0.8903</td>
    </tr>
    <tr>
        <td>LGBM</td>
        <td>0.9891</td>
        <td>0.9477</td>
    </tr>
    <tr>
        <td>CNN</td>
        <td>0.9531</td>
        <td>0.9210</td>
    </tr>
    <tr>
        <td>LSTM</td>
        <td>0.9900</td>
        <td>0.9701</td>
    </tr>
</table>


 <h3>Challenges:</h3>

<ul>
    <li>Sparsity of the Dataset</li>
    <li>A lot of missing values</li>
    <li>Imbalanced <code>isFraud</code> variable</li>
    <li>Outliers</li>
</ul>

 <b>LSTM gives the best CV auc results.</b>
