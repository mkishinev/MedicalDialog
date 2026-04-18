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

 
 **Who sees it?**
	→ You + the system and limited internal access inside the company which develops your AI system. 
 **Is it secure?**
	→ Yes, by modern cloud standards.
 **Is it fully private like a hospital record?**
	→ No — it’s not HIPAA-protected infrastructure. Privacy protection is not as strong as a hospital Electronic Medical Record system.
  
### How to maximize privacy 
  
  **Anonymize your data:**
  
    * Use pseudonyms instead of real names in medical history files.
	* Remove names and locations from all uploaded labs, scans, procedure reports when creating and updating medical history. 
	  If these reports are in PDF, you can use a PDF editor to modify the report before uploading (e.g., PDFgear).
	* Never include highly sensitive information like SSN, insurance IDs, date of birth, etc. 
	
### How to get more details 
  
  Ask your AI system regarding its data privacy and security, e.g.,
  > **User:** Who can see Nick's data? How secure the data is? What about privacy?

--- 
 
## Creation and update of the medical files
 
---
 
## Prompt optimization

Prompt optimization is about making your question easier for a model to reason about correctly — not just easier to read. 
The goal is to reduce ambiguity, control the scope, and guide the structure of the answer so you get something accurate, 
comparable, and useful rather than generic.

It is useful for a more productive dialog with an AI system to run your "raw" prompts through prompt optimization using 
the same (or different) AI system.

E.g., the first prompt of dialogs/dialog2 was obtained with ChatGPT as follows:

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