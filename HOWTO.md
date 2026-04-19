# Important details of using MedicalDialog

Here we discuss details on 
 * data privacy and security,
 * use of the AI system to simplify creation and updates of the medical files,
 * prompt optimization.
 
  
 ---
 
## Data privacy and security

 The data you upload and the chats are private to you, not publicly visible, not shared with other users. 
 The data you have uploaded is encrypted both in transit (while you interact with the AI system) 
 and at rest on cloud servers.

 **Caveat:** Conversations may be used to improve models through data training and limited human reviews at the developing company. 
 While you can turn off the permission to use your data for training in the setup of your AI system, 
 it comes with a significant drawback: your chats will be kept and available to you for a very limited time (72 hours instead of 18 months).  

 
 **Who sees it?** You + the system and limited internal access inside the company which develops the AI system.
	
 **Is it secure?** Yes, by modern cloud standards.
	
 **Is it fully private like a hospital record?** No — it’s not HIPAA-protected infrastructure. Privacy protection is not as strong as a hospital Electronic Medical Record system.
  
### How to maximize privacy 
  
  **Anonymize your data:**
  
    * Use pseudonyms instead of real names in medical history files.
	* Remove names and locations from all uploaded labs, scans, procedure reports when creating and updating medical history. 
	  If these reports are in PDF, you can use a PDF editor to modify the report before uploading (e.g., PDFgear).
	* Never include highly sensitive information like SSN, insurance IDs, exact date of birth, etc. 
	
### How to get more details 
  
  Ask your AI system regarding its data privacy and security, e.g.,
  > **User:** Who can see Nick's data? How secure the data is? What about data privacy?

--- 
 
## Creation and update of the medical files

Medical summary and medications files are created manually in a text editor.

More complex Imaging and procedures file and labs csv file are creted with the help of your MedicalDialog assistant.

### Medical summary file
Create medical summary file manually using the template in templates/medical_summary.md and med_history_example/medical_summary.md.
This file reflects major medical events that you remember or can find in your medical history. 

### Medication and treatments file
Create medicaions_and_treatements.md file manually using the template in templates/medications_and_treatements.md and med_history_example/medicaions_and_treatements.md
	* Put only recurring medications here. If a dentist prescribed you Tylenol for a few days after a dental procedure no need to include such short term meds.
    * If you stopped some meds do not remove the row from the table. Add "stopped" in the proper column instead.	

### Imaging and procedures file
Setup the MedicalDialog assistant with partially filled files as described in setup/. 
Add templates for imaging_and_procuders.md and labs.csv even if they are empty.
Go to your MedicalDialog assistant (project in ChatGPT and Claude or Gem in Gemini).

Let's say we want to add Nick's new_scan.pdf information. Conduct the following dialog:

 > **User:** Generate an md section for the imaging_and_procedures.md file based on the following imaging report.
   Upload new_scan.pdf alongside the above prompt.
  
  > **Assistant:**  (ChatGPT example)
  Here is a ready-to-append MD block for your Imaging_and_Procedures.md, formatted exactly per your schema and grounded strictly in the uploaded report.
  ```
  - study_type: "CT Coronary Artery Calcium Scoring (CAC)"
  body_region: "Coronary Arteries / Heart"
  exam_date: "2026-03-20"
  facility: "Regional Cardiovascular Imaging Center"
  indication: "ASCVD risk stratification; post-NSTEMI follow-up; statin therapy monitoring; history of PCI/stent to LAD (2021); elevated Lp(a)."
  technique: "Non-contrast ECG-gated CT of the chest using 64-slice multidetector CT; Agatston scoring method; 3mm contiguous axial slices during single breath-hold."
  key_findings:
    - "Calcified plaque predominantly in the left anterior descending artery (LAD)."
    - "Mild calcification in the left circumflex artery (LCX)."
    - "No calcification in the right coronary artery (RCA)."
    - "No pericardial effusion."
    - "No significant incidental pulmonary or mediastinal findings."
  quantitative_results:
    - name: "Total CAC Score"
      value: "142"
      units: "Agatston units"
      reference_or_interpretation: "Elevated; >75th percentile for age/sex; moderate atherosclerotic burden"
    - name: "LAD CAC Score"
      value: "118"
      units: "Agatston units"
      reference_or_interpretation: "Predominant vessel; consistent with prior PCI/stent"
    - name: "LCX CAC Score"
      value: "24"
      units: "Agatston units"
      reference_or_interpretation: "Mild calcification"
    - name: "RCA CAC Score"
      value: "0"
      units: "Agatston units"
      reference_or_interpretation: "No calcification detected"
    - name: "Risk Percentile"
      value: ">75th percentile"
      units: "Percentile"
      reference_or_interpretation: "Compared to males age 55–65 (MESA reference); indicates elevated 10-year ASCVD risk"
  impression: "Moderate coronary artery calcification (total CAC 142), predominantly in LAD, consistent with known ASCVD and prior PCI with drug-eluting stent. Mild LCX involvement; RCA without calcification. Overall high cardiovascular risk category."
  recommendations: "Continue high-intensity statin therapy (atorvastatin 40 mg) targeting LDL-C <70 mg/dL and ApoB <80 mg/dL; reassess CAC in 3–5 years or sooner if lipid targets unmet; address elevated Lp(a) with cardiology; continue aspirin 81 mg and ACE inhibitor; maintain high physical activity level."
  source_file: "CT CAC report 2026-03-20 (Regional Cardiovascular Imaging Center)"
  ```

Append this markdown section within the triple backticks (\```\) into the previous version of imaging_and_procedures.md file.

After updates are done upload it to your MedicalDialog Assistant in ChatGPT, Gemini, or Claude replacing the prior version. 


### Labs file
 
---
 
## Prompt optimization

Prompt optimization makes your question easier for a model to reason about correctly — not just easier to read. 
The goal is to reduce ambiguity, control the scope, and guide the structure of the answer so you get something accurate, 
comparable, and useful rather than generic.

for a more productive dialog with an AI system it is useful  to run your "raw" prompts through prompt optimization using 
the same (or different) AI system.

E.g., the first prompt of dialogues/dialog2 was obtained with ChatGPT as follows:

  > **User:** Optimize the following prompt:
  ```
  Given the following: 
  - Nick's history of cardiovascular problem and high cardiovascular risk 
  - LDL and ApoB are out of range in the latest lipid panel 
  - Lp(a) is out of range. 
  
  Nick feels that he needs to adjust his lipid medications. 
  
  - What type of medication adjustments are possible? 
  - What is their expected reduction in LDL-C and ApoB? 
  - What are their pros and cons?
  ```
  
  > **Assistant:**
  ```
  Given:

	- Established atherosclerotic cardiovascular disease (ASCVD)
	- Elevated LDL-C, ApoB, and Lp(a) on the latest lipid panel

  Evaluate evidence-based options to intensify lipid-lowering therapy.

  For each option (e.g., statin intensification, ezetimibe, PCSK9 inhibitors, bempedoic acid, inclisiran):

	- Expected % reduction in LDL-C and ApoB
	- Effect on Lp(a) (if any)
	- Mechanism of action
	- Clinical outcome evidence (CV events, mortality if available)
	- Pros and cons (efficacy, safety, cost, convenience)

	Conclude with:

	- A ranked strategy for a very high-risk patient
	- Typical target ranges for LDL-C and ApoB in this context
  ```

 
---
 
## How many MedicalDialog assistants do I need?
 
 If you want to have medical dialogues for more than one person, e.g., for members of your family, 
 you need to setup an assistant per person.