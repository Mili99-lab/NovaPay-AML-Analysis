<div align="center">
  <img width="300px" src="https://copilot.microsoft.com/th/id/BCO.8f18e85d-c6ff-46c9-8b7c-2229896f7848.png" />
</div>
<h1 align="center">NovaPay Financial — AML Transaction Intelligence Report</h1>
<table align="center">
  <tr>
    <td width="1440">
      <h2 align="center">Client Background</h2>
      <body>
        <strong>Novapay</strong> Financial is a fast‑growing fintech platform specializing in mobile money transfers and digital payments. Established in 2018 to serve a diverse customer base across multiple regions and quickly scaled to processing millions of transactions each month. With five transaction types — CASH_IN, CASH_OUT, DEBIT, PAYMENT, and TRANSFER — the company became a trusted channel for everyday financial activity, from bill payments to peer‑to‑peer transfers. <br>
<br>
As <strong>Novapay</strong> expanded, so did the complexity of its compliance obligations. The company’s rule‑based fraud detection system, designed to flag suspicious activity, began to show cracks under the weight of scale. Thousands of alerts were generated daily, overwhelming the compliance team, yet the system was still missing the majority of actual fraud cases. This imbalance created a dual challenge of wasted analyst effort on false alarms and billions of dollars in undetected fraudulent exposure.<br>
<br>
Recognizing the urgency, <strong>Novapay's</strong> leadership commissioned a deep‑dive analysis into its transaction data. Over a 30‑day period, 6.3 million records were examined to uncover hidden fraud patterns, evaluate the effectiveness of the existing detection system, and propose actionable improvements. The goal was clear — to transform compliance monitoring from a reactive, rule‑bound process into a proactive intelligence framework capable of identifying high‑risk behaviors before they escalate. The key insights and recommendations focus on the following areas:
      </body>
      <h3>Northstar Metrics</h3>
      <h4>
        <ul><li>Fraud Detection Performance - Focuses on measuring how effectively NovaPay’s existing rule-based system identifies fraudulent transactions.</li>
          <li>Transaction Risk Distribution – Focuses on identifying which transaction types (TRANSFER, CASH_OUT, etc.) carry the highest fraud exposure.</li>
          <li>Behavioral Fraud Signals – Focuses on uncovering patterns that indicate fraudulent intent, such as balance wipe-outs or high-velocity transfers.</li>
          <li>Customer Risk Segmentation – Focuses on classifying customers into risk tiers (Critical, High, Medium, Low) based on transaction behavior.</li>
          <li>Financial Exposure Analysis – Focuses on quantifying the total transaction volume linked to undetected fraud.</li>
        </ul>
      </h4>
    </td>
  </tr>
</table>
<table align="center">
  <tr>
      <h1 align="center">Executive Summary</h1>
     <h3 align="center">Fraud Detection Overview (30‑Day Analysis)</h3>
    <div align="center">
  <table>
    <tr>
      <td>
         <img width="2085" height="1035" alt="chart7_executive_summary" src="https://github.com/user-attachments/assets/88f1e727-f5a6-4188-9c17-a704740efe85" />
      </td>
    </tr>
  </table>
</div> 
        <ol>
          <li>
            <strong>Compliance System Performance:</strong>
            <ul>
              <li>Evaluated over a 30‑day period covering 6.36 million transactions across five payment channels which revealed that the existing rule‑based alert mechanism is severely underperforming.</li>
              <li>Achieving a recall of only 0.19%, correctly identifying just 16 of 8,213 confirmed fraud cases.</li>
              <li>Underscores a critical gap in the company’s anti‑money‑laundering (AML) framework, where thousands of fraudulent activities remain undetected each month.</li>
            </ul>
          </li>
          <li>
            <strong>High‑Risk Transaction Channels</strong>
            <ul>
              <li>Fraud is highly concentrated in TRANSFER and CASH_OUT transactions, which together account for all confirmed fraud cases.</li>
              <li>TRANSFER alone exhibits a fraud rate of 0.769%, nearly four times higher than CASH_OUT (0.184%).</li>
              <li>Other transaction types — PAYMENT, DEBIT, and CASH_IN — show zero fraud incidence, suggesting that compliance monitoring should be strategically narrowed to high‑risk channels.</li>
            </ul>
          </li>
        </ol>
          <li>
            <strong>Behavioral Pattern Insights</strong>
            <ul>
              <li>Accounts draining to zero before a transfer or cash‑out show a 0.67% fraud rate, 67× higher than normal accounts.</li>
<li>Rapid consecutive transfers within short time windows correlate strongly with fraud clusters.</li>
<li>Outlier transactions exceeding historical averages often precede account closure or inactivity.</li>
<li>These behavioral markers form the foundation for a behavioral scoring model projected to improve detection recall by 70%+ while maintaining precision.</li>
            </ul>
          </li>
<li>
            <strong>Customer Risk Segmentation</strong>
            <ul>
              <li>Risk profiling classified 8,053 accounts as CRITICAL, requiring immediate Suspicious Activity Report (SAR) review.</li>
              <li> An additional 2.48 million accounts fall under the medium‑risk tier, warranting periodic monitoring.2</li>
              <li>This segmentation enables NovaPay’s compliance team to prioritize investigations and allocate resources efficiently.</li>
            </ul>
          </li>
<li>
            <strong>Financial Exposure</strong>
            <ul>
              <li>The analysis estimates $12.06 billion in transaction volume linked to undetected fraud, representing a 0.13% exposure rate.</li>
              <li>Provides a tangible measure of the financial and regulatory risk posed by the current detection inefficiencies.</li>
            </ul>
          </li>
<li>
            <strong>Strategic Implications</strong>
            <ul>
              <li>The findings advocate for replacing NovaPay’s static rule‑based system with a dynamic behavioral scoring model that integrates transaction type, balance behavior, and velocity metrics.</li>
              <li>Concentrating alerts on TRANSFER and CASH_OUT transactions alone could reduce analyst workload by ~55%, while implementing balance wipe‑out triggers would immediately elevate detection accuracy.</li>
            </ul>
          </li>
          </ol>
  </tr>
</table>
<h2 align="center">Dataset Structure and ERD (Entity relationship diagram)</h2>
<body>The AML database was designed to store and analyze 6.36 million transactions across five payment types. The structure integrates raw transaction records, fraud labels, and customer segmentation outputs, enabling both SQL queries and behavioral analysis.</body>
<div align="center">
  <img width="680" src="https://copilot.microsoft.com/th/id/BCO.cd98cca0-3114-402e-b99a-6300a3867dc9.png">
</div>
<h1 align="center">Insights Deep-Dive</h1>
<table align="center">
  <tr>
    <h1 align="center">Transaction Risk Distribution</h1>
    <td width="1000">
      <img width="2084" height="925" alt="chart1_transaction_overview" src="https://github.com/user-attachments/assets/4579cea4-30fc-4383-ba30-46b5086fdde4" />
    </td>
  </tr>
</table>
<table>
  <tr>
    <td>
      <strong>Transaction Risk Distribution</strong>
      <ol>
        <li>Analysis of 6.36 million transactions revealed that fraud is highly concentrated within just two transaction types: TRANSFER and CASH_OUT. Together, these channels account for virtually all confirmed fraud cases across the NovaPay ecosystem.</li>

 <li>TRANSFER transactions emerged as the highest-risk channel with a fraud rate of 0.769%, making them approximately four times riskier than CASH_OUT transactions, which recorded a fraud rate of 0.184%.</li>

 <li>In contrast, PAYMENT, CASH_IN, and DEBIT transactions showed zero fraud incidence across more than 3.6 million transactions, indicating that fraudsters deliberately avoid these transaction channels.</li>

<li>The findings suggest that fraudsters prioritize transaction methods that enable rapid movement of funds between accounts while minimizing opportunities for intervention by compliance teams.</li>

<li>A recurring fraud pattern was observed where funds were initially transferred to secondary accounts and subsequently withdrawn through CASH_OUT transactions, forming a consistent laundering pathway.</li>

<li>Current monitoring efforts are distributed across all transaction types equally, resulting in unnecessary investigative effort being spent on channels with historically negligible fraud risk.</li>

<li>By concentrating monitoring efforts on TRANSFER and CASH_OUT transactions, NovaPay can significantly improve detection efficiency while reducing alert fatigue for compliance analysts.</li>

<li>This analysis establishes transaction type as one of the strongest predictors of fraud risk and a critical feature for future fraud scoring models.</li>
  </ul>
</li>

<li>Operational Outcome
  <ul>
    <li>Reduced analyst workload through risk-based monitoring.</li>
    <li>Improved fraud detection efficiency.</li>
    <li>Enhanced allocation of compliance resources.</li>
    <li>Supports development of transaction-specific fraud models.</li>
  </ul>
</li>   
    </td>
  </tr>
</table>
<div align="center">
  <table>
    <tr>
       <td width="1000" valign="top">
      <img width="2085" height="1183" alt="chart3_hourly_trend" src="https://github.com/user-attachments/assets/20fa033c-02fe-4bdd-bdb6-bd80ab87e147" />
    </td>
    </tr>
  </table>
</div>
<table align="center">
  <tr>
     <h1 align="center">Behavioral Fraud Signals</h1>
      <div align="center">
        <img width="2085" height="889" alt="chart4_balance_wipeout" src="https://github.com/user-attachments/assets/b2cd2e1d-f05f-45c1-a3b9-ded15b22e4e0" />
      </div>
    <tr>
  </tr>
</table>
<table aign="center">
  <tr>
    <li>While transaction type identifies where fraud occurs, behavioral analysis explains how fraudsters operate before fraudulent transactions are executed.</li>
    <li>The strongest fraud indicator identified was the Balance Wipe-Out Pattern, where accounts transferred or withdrew nearly their entire available balance in a single transaction.</li>
    <li>Accounts exhibiting balance wipe-out behavior recorded a fraud rate of approximately 0.67%, compared with only 0.01% among accounts retaining positive balances after transactions.</li>
    <li>This behavior makes balance wipe-out events approximately 67 times more predictive of fraud than randomly selecting transactions for investigation.</li>
    <li>Fraudulent accounts frequently demonstrated high transaction velocity, executing multiple transfers within short time intervals before cashing out funds.</li>
    <li>The velocity pattern suggests fraudsters operate against time, attempting to move funds before customers report suspicious activity or security controls intervene.</li>
    <li>Another recurring signal involved transaction amount anomalies, where fraudulent transactions significantly exceeded customers' historical transaction averages.</li>
    <li>These behavioral indicators consistently appeared across confirmed fraud cases regardless of transaction amount thresholds, demonstrating the limitations of static rule-based monitoring.</li>
    <li>The findings indicate that customer behavior provides significantly stronger fraud signals than transaction value alone and should become the foundation of future fraud detection strategies.</li>

<li>Operational Outcome
  <ul>
    <li>Provides a framework for behavioral fraud scoring.</li>
    <li>Enables earlier fraud identification before financial losses occur.</li>
    <li>Improves fraud recall while maintaining manageable investigation volumes.</li>
    <li>Creates a scalable detection strategy that adapts to evolving fraud techniques.</li>
  </ul>
</li>
      </td>
</tr>
</table>
<table align="center">
    <tr align="center">
    <td width="1000">
      <img width="2077" height="886" alt="chart6_system_quality" src="https://github.com/user-attachments/assets/26cb0629-cae0-40f9-8a4d-3c70fbd0e8e3" />
    </td>
  </tr>
</table>


</table>
<table align="center">
  <tr>
    <h1 align="center">Customer Risk segmentation</h1>
    <table align="center">
    <tr align="center">
      <td width="1000">
      <img width="1958" height="889" alt="chart5_risk_tiers" src="https://github.com/user-attachments/assets/b12282a8-4df0-409d-a4ed-3b04655163fa" />
    </td>
  </tr>
</table>
    <table>
      <tr>
        <td>
    <li>To improve investigative efficiency, customer accounts were segmented into four risk tiers based on fraud indicators, transaction behavior, and historical activity patterns.</li>
    <li>A total of 8,053 accounts were classified as CRITICAL risk due to confirmed fraud activity and repeated high-risk behavioral indicators.</li>
    <li>These accounts require immediate Suspicious Activity Report (SAR) review and represent the highest concentration of compliance risk within the customer base.</li>
    <li>An additional 160 accounts were classified as HIGH risk after demonstrating multiple suspicious behavioral characteristics associated with confirmed fraud patterns.</li>
    <li>Approximately 2.48 million accounts were categorized as MEDIUM risk, exhibiting occasional risk indicators but lacking sufficient evidence for immediate escalation.</li>
    <li>273,263 accounts were identified as LOW risk due to stable transaction histories and minimal fraud-related behavioral signals.</li>
    <li>The analysis revealed that fraud risk is concentrated within a relatively small proportion of customers, creating an opportunity for targeted investigation strategies.</li>
    <li>Risk segmentation allows compliance teams to prioritize reviews based on fraud probability rather than transaction volume, significantly improving investigative productivity.</li>
    <li>This framework enables NovaPay to transition from reactive fraud investigations toward proactive risk management.</li>

<li>Operational Outcome
  <ul>
    <li>Prioritizes investigative efforts toward highest-risk customers.</li>
    <li>Reduces review times and improves case management efficiency.</li>
    <li>Supports regulatory reporting and SAR workflows.</li>
    <li>Creates a scalable customer risk monitoring framework.</li>
  </ul>
</li>
        </td>
      </tr>
    </table>
  </tr>
</table>
<table align="center">
  <h1 align="center">Financial Exposure Analysis</h1>
  <tr>
    <td width="500">
       <div valign="top" align="center">
      <img width="2085" height="742" alt="chart2_amount_distribution" src="https://github.com/user-attachments/assets/96587c7b-6131-45fd-8b22-4c40aa8551df" />
    </div>
    </td>
    <td valign="top" width="500">
    <li>The analysis estimated approximately $12.06 billion in transaction volume linked to fraudulent activity that remained undetected by NovaPay's existing monitoring framework.</li>
    <li>Although representing only 0.13% of total transaction volume, the absolute value of undetected fraud exposure presents substantial financial, regulatory, and reputational risk.</li>
    <li>The primary driver of this exposure is the system's extremely low fraud recall rate of 0.19%, resulting in 8,197 confirmed fraud cases bypassing detection controls.</li>
    <li>For every fraudulent transaction successfully detected, more than 500 fraudulent transactions remained undetected, highlighting a significant weakness in the current compliance framework.</li>
    <li>Fraud activity remained remarkably consistent throughout the 30-day analysis period, averaging approximately 11 fraud cases per hour with peak periods exceeding 40 cases within a single hour.</li>
    <li>The absence of strong daily or weekly seasonality suggests that fraud is an ongoing operational threat rather than an isolated event driven by specific time windows.</li>
    <li>This finding reduces the effectiveness of time-based detection rules and reinforces the need for behavior-driven monitoring strategies.</li>
    <li>If left unresolved, continued growth in transaction volume will likely increase undetected fraud exposure and elevate regulatory scrutiny.</li>
    <li>The findings demonstrate that the greatest organizational risk is not detected fraud, but rather the billions of dollars in fraudulent activity that currently remain invisible to compliance systems.</li>

<li>Operational Outcome
  <ul>
    <li>Quantifies the financial impact of ineffective fraud detection.</li>
    <li>Supports investment decisions for advanced monitoring solutions.</li>
    <li>Provides executive visibility into compliance risk exposure.</li>
    <li>Establishes measurable benchmarks for future fraud reduction initiatives.</li>
  </ul>
</li>
    </td>
  </tr>
</table>
  <tr>
    <td width="700" border="0"><h1>Key Strategic Recommendation</h1>
    <h4>Based on the uncovered insights, here are actionable items that TechSphere can take away from our analysis.</h4></td>
    <td width="400" border="0"><div align="right">
    </div></td>
  </tr>
</table>
<table align="center">
    <li>The existing rule-based fraud detection system prioritizes precision over recall, resulting in a 99.8% fraud miss rate and exposing the organization to significant financial risk.</li>
    <li>A behavioral fraud scoring framework leveraging transaction type risk, balance wipe-out behavior, transaction velocity, and amount anomaly detection is recommended as the next stage of NovaPay's fraud monitoring maturity.</li>
    <li>Based on the signal strength observed throughout the analysis, implementing these behavioral indicators could improve fraud detection recall by more than 70% while simultaneously reducing compliance investigation workload.</li>
    <li>Focusing analyst attention on TRANSFER, CASH_OUT, and CRITICAL-risk accounts would provide the highest return on investigative effort and materially reduce fraud exposure.</li>
  </ul>
</li>
</table>
