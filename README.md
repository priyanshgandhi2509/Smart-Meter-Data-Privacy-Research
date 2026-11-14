# ⚡ Smart Meter Data Privacy and Protection: Problem Identification and Background Research

[![Standard](https://img.shields.io/badge/Format-IEEE_Conference_Template-00629B.svg?style=flat-square&logo=ieee&logoColor=white)](https://www.ieee.org/)
[![Domain](https://img.shields.io/badge/Domain-Cyber--Physical_Systems_%26_IoT_Privacy-orange.svg?style=flat-square)](https://www.ncirl.ie/)
[![Lead Author](https://img.shields.io/badge/Lead_Author-Priyansh_Gandhi-darkgreen.svg?style=flat-square)](https://github.com/priyanshgandhi2509)
[![UN SDGs](https://img.shields.io/badge/UN_SDGs-7%20%7C%209%20%7C%2011%20%7C%2012-blue.svg?style=flat-square)](https://sdgs.un.org/goals)
[![Institution](https://img.shields.io/badge/Institution-National_College_of_Ireland-003366.svg?style=flat-square)](https://www.ncirl.ie/)

---

## 📖 Research Abstract

Electric utilities worldwide are replacing legacy electromechanical meters with **Advanced Metering Infrastructure (AMI)** smart meters. While high-frequency telemetry (1 to 15-minute sampling) is essential for balancing intermittent renewable energy sources (wind and solar) and executing dynamic demand-response, it introduces a critical cyber-physical privacy vulnerability. 

Every household electrical appliance possesses a distinct current and voltage signature. By applying **Non-Intrusive Load Monitoring (NILM)** algorithms to aggregate domestic consumption traces, unauthorized third parties, state adversaries, or compromised utility servers can reverse-engineer private domestic activities. This paper investigates the technical root causes of AMI telemetry leakage, evaluates consumer risk across physical security and medical confidentiality, maps privacy solutions to **United Nations Sustainable Development Goals (SDGs)**, and synthesizes modern technical countermeasures including **homomorphic encryption**, **verifiable zero-knowledge proofs**, and **battery load buffering**.

---

## 🔍 The Core Problem: NILM Appliance Disaggregation

```
[Domestic Household]  ──>  [Aggregated Load Signature]  ──>  [NILM Disaggregation]
   • Refrigerator (Compressor cycles)                          │
   • Electric Kettle (1500W transient spike)                  ├──> Detailed Domestic Profile:
   • Microwave (Magnetron harmonics)                          │    • Sleep & wake schedules
   • CPAP / Medical Pump (Distinct power draw)                │    • Absence & vacation tracking
   • EV Charger (Continuous high-current block)               │    • Medical condition inference
```

### Critical Privacy Threats Identified:
1. **Burglary and Absence Tracking**: Continuous drops to baseline power (80–100W) reveal unattended residences in real-time, creating acute physical security risks.
2. **Behavioral & Sleep Routine Profiling**: High-frequency telemetry exposes exact waking, sleeping, cooking, and entertainment habits.
3. **Medical & Health Confidentiality Breaches**: Specialized medical devices (e.g. CPAP machines, oxygen concentrators, home dialysis equipment) exhibit unmistakable load profiles, leaking confidential medical conditions without consent.
4. **Commercial Surveillance & Dynamic Price Discrimination**: Data brokers and advertising conglomerates can exploit domestic habits for invasive behavioral monetization.

---

## 🌍 Alignment with United Nations Sustainable Development Goals (SDGs)

| UN SDG | Goal Title | Technical Relevance to Smart Meter Privacy |
| :---: | :--- | :--- |
| **SDG 7** | Affordable and Clean Energy | Builds consumer trust in demand-response and dynamic pricing, accelerating clean energy transition without fear of domestic surveillance. |
| **SDG 9** | Industry, Innovation, and Infrastructure | Hardens critical electrical grid infrastructure against data-mining attacks, eavesdropping, and cyber-physical compromises. |
| **SDG 11** | Sustainable Cities and Communities | Prevents smart urban grids and IoT sensor networks from transforming into involuntary civilian surveillance platforms. |
| **SDG 12** | Responsible Consumption and Production | Empowers consumers with transparent consumption analytics while cryptographically safeguarding their right to privacy. |

---

## 🛡️ Technical & Cryptographic Countermeasures

```
                    ┌────────────────────────────────────────────────────────┐
                    │               ARCHITECTURAL SEPARATION                 │
                    └──────────────────────────┬─────────────────────────────┘
                                               │
             ┌─────────────────────────────────┴─────────────────────────────────┐
             ▼                                                                   ▼
┌───────────────────────────┐                                       ┌───────────────────────────┐
│ HIGH-FREQUENCY TELEMETRY  │                                       │   MONTHLY BILLING DATA    │
├───────────────────────────┤                                       ├───────────────────────────┤
│ • Paillier Homomorphic    │                                       │ • Aggregated Cumulative   │
│   Encryption (E[x] * E[y])│                                       │   Kilowatt-Hour Totals    │
│ • Spatial Feeder-Level    │                                       │ • Zero-Knowledge Proofs   │
│   Aggregation             │                                       │   of Dynamic Tariff Sum   │
│ • Anonymous Grid State    │                                       │ • Identity-Linked Billing │
└───────────────────────────┘                                       └───────────────────────────┘
```

1. **Spatial Homomorphic Aggregation**:
   - Smart meters encrypt high-frequency operational telemetry using additive homomorphic cryptosystems (e.g., **Paillier cryptosystem**).
   - Intermediate substations aggregate encrypted values ($E(m_1) \cdot E(m_2) = E(m_1 + m_2)$) without ever decrypting individual household traces.
2. **Verifiable Zero-Knowledge Proofs (ZKPs)**:
   - Enables meters to prove mathematically that time-of-use tariffs were calculated correctly without sending unencrypted timestamped interval data.
3. **Physical Battery Energy Storage System (BESS) Buffering**:
   - Hardware-level load signature masking: Local battery units dynamically inject or absorb power to flatten appliance-induced spikes, completely denying NILM classifiers the high-frequency features needed for disaggregation.

---

## 📑 Research Deliverables & Assets

* 📄 `Smart_Meter_Data_Privacy_IEEE_Report.pdf`: Final IEEE two-column formatted conference research publication.
* 📝 `Smart_Meter_Data_Privacy_IEEE_Report.docx`: Fully formatted IEEE source document with metadata, tables, and references.
* 📊 `Smart_Meter_Data_Privacy_Presentation.pptx`: Academic defense presentation deck outlining problem identification, sustainability benchmarks, and architectural solutions.

---

## 👨‍💻 Research Team & Acknowledgments

* **Lead Author**: **Priyansh Gandhi**
* **Institution**: National College of Ireland (NCI) — School of Computing
* **Programme**: Master of Science in Cybersecurity
* **GitHub**: [@priyanshgandhi2509](https://github.com/priyanshgandhi2509)
