# Fraud-Detection

<H3>Overview</H3>

This repository contains the code and analysis for a fraud detection . The goal was to classify whether a transaction was fraudulent based on transactional and identity data. The dataset consisted of approximately 590,540 training samples (3.5% fraud) and 506,691 test samples.

<h3>Dataset</h3>
IEEE-CIS Fraud Detection Kaggle competition Dataset is used.
TransactionDT: Timedelta from a given reference datetime (not an actual timestamp), but the time difference in seconds from a certain time.
TransactionAMT: Transaction payment amount in USD, the decimal part is worth paying attention to.
ProductCD: Product code, the product for each transaction. It may not necessarily be an actual product but may also refer to a service.
card1-card6: Payment card information, such as card type, card category, issue bank, country, etc.
addr1-addr2: Address, billing region and billing country
dist: Distances between (not limited) billing address, mailing address, zip code, IP address, phone area, etc.
P_ and (R__) emaildomain: Purchaser and recipient email domain, some transactions do not require the recipient, and the corresponding Remaildomain is empty
C1-C14: Counting, such as how many addresses are found to be associated with the payment card, etc.
D1-D15: Timedelta, such as days between previous transaction, etc.
M1-M9: Match, such as names on card and address, etc.
Vxxx: Vesta engineered rich features, including ranking, counting, and other entity relations. Some V features are missing in different proportions.
