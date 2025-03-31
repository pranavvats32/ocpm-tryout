# Object-Centric Process Mining (OCPM) Tryout

This project explores Object-Centric Process Mining (OCPM) using datasets from the OCPA GitHub repository. The analysis involves process discovery, variant filtering, and process conformance (precision and fitness).

## Datasets Used
- **P2P Dataset**: A purchase-to-pay example log.
  Number of process executions: 516
  Number of variants: 315
  Objects Involved: 7 (Purchase Order, Quotation, Material, Goods 
  Receipt, Payment, Purchase Requisition, Invoice Receipt)
- **Intermediate Dataset**: A sample intermediate event log.
  Number of process executions: 1000
  Number of variants: 917
  Objects Involved: 2 (Application and Offer)
## Features Implemented
### 1. Process Discovery
- Imported event logs in **JSONOCEL** format.
- Discovered Object-Centric Petri Nets (OCPNs) using `ocpa.algo.discovery.ocpn`.
- Visualized the discovered process models.

### 2. Variant Filtering
- Extracted process execution variants.
- Computed layout coordinates for process variants.
- Displayed key statistics (number of process executions and variants).

### 3. Process Conformance
- Evaluated **Precision** and **Fitness** to assess model quality.
- Compared event log behavior with discovered models.

## Installation
### Prerequisites
Ensure you have Python installed (version 3.8+ recommended).

### Install Dependencies
Run the following command to install the required libraries:
```bash
pip install ocpa 
```
Prefarabely in conda prompt using admin priviledge.

## Known Issues
- **Conformance**: Fitness and precision of the full log cannot be calculated, log needs to be filtered by removing infrequent variants.
- **JSON vs. JSONOCEL format mismatch**: The datasets on the OCPA website may require conversion.
- **Visualization scaling**: The complete log produces a Petri net that is too large to be easily readable.
  
## Future Improvements
- Implement additional conformance checking techniques.
- Explore object-token-based replay for better fitness evaluation.

## References
- [OCPA GitHub Repository](https://github.com/ocpm/ocpa)
- [OCPM Documentation](https://ocpa.readthedocs.io/en/latest/)
- [OCPI](https://ocpi.ai/#about)
- [P2P Log]([https://ocpi.ai/#about](https://github.com/ocpm/ocpa/blob/main/sample_logs/jsonocel/p2p-2023.jsonocel))
- [Intermediate Log](https://github.com/ocpm/ocpa/blob/main/sample_logs/jsonocel/intermediate.jsonocel)



