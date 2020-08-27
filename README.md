# UCI_Bank_Marketing
Project from "https://archive.ics.uci.edu/ml/index.php"

1. Title: Bank Marketing (with social/economic context)

2. Sources

Created by: Sérgio Moro (ISCTE-IUL), Paulo Cortez (Univ. Minho) and Paulo Rita (ISCTE-IUL) @ 2014

3. Past Usage:

The full dataset (bank-additional-full.csv) was described and analyzed in:

S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems (2014), doi:10.1016/j.dss.2014.03.001.

4. Relevant Information:

This dataset is based on &quot;Bank Marketing&quot; UCI dataset (please check the description at: http://archive.ics.uci.edu/ml/datasets/Bank+Marketing).

The data is enriched by the addition of five new social and economic features/attributes (national wide indicators from a ~10M population country), published by the Banco de Portugal and publicly available at: https://www.bportugal.pt/estatisticasweb.

This dataset is almost identical to the one used in [Moro et al., 2014] (it does not include all attributes due to privacy concerns).

Using the rminer package and R tool (http://cran.r-project.org/web/packages/rminer/), we found that the addition of the five new social and economic attributes (made available here) lead to substantial improvement in the prediction of a success, even when the duration of the call is not included. Note: the file can be read in R using: d=read.table(&quot;bank-additional-full.csv&quot;,header=TRUE,sep=&quot;;&quot;)

The zip file includes two datasets:

1) bank-additional-full.csv with all examples, ordered by date (from May 2008 to November 2010).

2) bank-additional.csv with 10% of the examples (4119), randomly selected from bank-additional-full.csv.

The smallest dataset is provided to test more computationally demanding machine learning algorithms (e.g., SVM).

The binary classification goal is to predict if the client will subscribe a bank term deposit (variable y).

5. Number of Instances: 41188 for bank-additional-full.csv

6. Number of Attributes: 20 + output attribute.

7. Attribute information:

For more information, read [Moro et al., 2014].

Input variables:

# bank client data:

1 - age (numeric)

2 - job : type of job (categorical: &quot;admin.&quot;,&quot;blue-collar&quot;,&quot;entrepreneur&quot;,&quot;housemaid&quot;,&quot;management&quot;,&quot;retired&quot;,&quot;self-employed&quot;,&quot;services&quot;,&quot;student&quot;,&quot;technician&quot;,&quot;unemployed&quot;,&quot;unknown&quot;)

3 - marital : marital status (categorical: &quot;divorced&quot;,&quot;married&quot;,&quot;single&quot;,&quot;unknown&quot;; note: &quot;divorced&quot; means divorced or widowed)

4 - education (categorical: &quot;basic.4y&quot;,&quot;basic.6y&quot;,&quot;basic.9y&quot;,&quot;high.school&quot;,&quot;illiterate&quot;,&quot;professional.course&quot;,&quot;university.degree&quot;,&quot;unknown&quot;)

5 - default: has credit in default? (categorical: &quot;no&quot;,&quot;yes&quot;,&quot;unknown&quot;)

6 - housing: has housing loan? (categorical: &quot;no&quot;,&quot;yes&quot;,&quot;unknown&quot;)

7 - loan: has personal loan? (categorical: &quot;no&quot;,&quot;yes&quot;,&quot;unknown&quot;)

# related with the last contact of the current campaign:

8 - contact: contact communication type (categorical: &quot;cellular&quot;,&quot;telephone&quot;)

9 - month: last contact month of year (categorical: &quot;jan&quot;, &quot;feb&quot;, &quot;mar&quot;, ..., &quot;nov&quot;, &quot;dec&quot;)

10 - day\_of\_week: last contact day of the week (categorical: &quot;mon&quot;,&quot;tue&quot;,&quot;wed&quot;,&quot;thu&quot;,&quot;fri&quot;)

11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y=&quot;no&quot;). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

# other attributes:

12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)

13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)

14 - previous: number of contacts performed before this campaign and for this client (numeric)

15 - poutcome: outcome of the previous marketing campaign (categorical: &quot;failure&quot;,&quot;nonexistent&quot;,&quot;success&quot;)

# social and economic context attributes

16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)

17 - cons.price.idx: consumer price index - monthly indicator (numeric)

18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)

19 - euribor3m: euribor 3 month rate - daily indicator (numeric)

20 - nr.employed: number of employees - quarterly indicator (numeric)

Output variable (desired target):

21 - y - has the client subscribed a term deposit? (binary: &quot;yes&quot;,&quot;no&quot;)

8. Missing Attribute Values: There are several missing values in some categorical attributes, all coded with the &quot;unknown&quot; label. These missing values can be treated as a possible class label or using deletion or imputation techniques.
