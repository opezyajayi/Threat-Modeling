Overview

Threat modeling is a proactive cybersecurity practice used to identify, understand, and mitigate potential threats early in the system development lifecycle.
This project provides:

Structured data flow diagrams (DFDs)

Importable Threat Dragon JSON models

Microsoft TMT documentation and PDFs

Examples of STRIDE-based threat analysis

Guidance for building repeatable threat modeling workflows

🧰 Tools Used
🟦 OWASP Threat Dragon (v2.x)

An open-source threat modeling tool supporting browser and desktop versions.

Features used in this project:

Level 1–3 Data Flow Diagrams

Threat definitions based on OWASP Top 10 & STRIDE

Import/export of JSON models

Visual modeling using drag-and-drop elements

Output to documentation (PDF/Markdown)

Useful Links:

https://owasp.org/www-project-threat-dragon/

🟩 Microsoft Threat Modeling Tool (TMT)

A Windows-based enterprise tool for STRIDE threat analysis and security requirement generation.

Features used:

Automated threat generation

STRIDE-per-element analysis

Detailed mitigation recommendations

Threat and model exports (.tm7, .pdf)

Useful Links:

https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool

🧩 Project Structure
/threat-models
   ├── threatdragon/
   │     ├── Level1_Context.json
   │     ├── Level2_DFD.json
   │     ├── Level3_Workflow.json
   │     └── exports/
   │           └── DFD_Diagram.pdf
   │
   ├── microsoft-tmt/
   │     ├── Level2_DFD_Report.pdf
   │     ├── TMT_Model.tm7 (optional)
   │     └── STRIDE_Analysis.xlsx
   │
   └── docs/
         ├── threat_model_overview.md
         ├── mitigations.md
         └── architecture_summary.md

🛠 How to Use This Repository
1. View the Diagrams

All architecture and data flow diagrams are available in /docs and /threat-models/*/exports/.

2. Import Models into Threat Dragon

Launch Threat Dragon

Select Import Model → Upload JSON

Choose any .json file in /threat-models/threatdragon/

3. Use Models in Microsoft Threat Modeling Tool

Open Microsoft TMT

Import the .tm7 file (if included) or recreate the diagram using the provided PDF

Run Generate All Threats

Export mitigations or threat reports as needed

🔎 Threat Modeling Approach

This project follows a structured, repeatable approach:

1. Define Scope

Identify assets

Determine trust boundaries

List system components

2. Create DFDs (Levels 1–3)

Level 1: Context diagram

Level 2: Component interactions

Level 3: Detailed workflow (e.g., login, order placement)

3. Apply STRIDE
Category	Threat
S	Spoofing
T	Tampering
R	Repudiation
I	Information Disclosure
D	Denial of Service
E	Elevation of Privilege
4. Identify Mitigations

Authentication hardening

Input validation

Secure communication

Database access controls

Logging & monitoring

5. Document Findings

Export from Threat Dragon

Export STRIDE report from Microsoft TMT

Consolidate in /docs

📄 Included Outputs

✔ DFD diagrams (PDF)
✔ Threat Dragon JSON models
✔ Microsoft TMT PDF report
✔ STRIDE threat tables
✔ Mitigation recommendations

🚀 Future Improvements

Add automated threat generation (PyTM, Threagile)

Support cloud-specific models (AWS, Azure, GCP)

Integrate CI/CD security scanning models

Add architectural risk scoring

🤝 Contributing

Contributions are welcome!
If you'd like to extend the models, add new diagrams, or improve documentation:

Fork the repo

Create a feature branch

Submit a pull request
