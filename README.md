# MedicalDialog

A template and workflow for using AI assistants to prepare for medical appointments and understand your health records.

What this is: A set of template files and setup instructions that help you have better, more informed conversations with your doctor — not a substitute for one.

What this is not: Medical advice, a diagnostic tool, or an emergency resource. In a medical emergency, call 911 or your local emergency number.

## The problem

Most people walk into medical appointments underprepared. Symptoms get forgotten under pressure, lab results arrive with no context, and the 15 minutes with a doctor disappears before you've asked what you needed to ask. Doctors spend a significant portion of each appointment on basic Q&A that a prepared patient wouldn't need.

## What MedicalDialog does

You maintain a structured personal health files. 

If you receive new medical information from doctor visits, tests, or hospital visits you update the files to always keep information current. 

Before and after doctor appointments, you have a dialog with an AI assistant to:

* Generate a concise summary of your current situation
* Prepare a focused list of questions for your doctor
* Interpret lab results and test reports in plain language
* Track how your health picture changes over time
* Discuss pros and cons of different medications and how medications interact with each other or your conditions.

Works with Claude Projects, Gemini Gems, and ChatGPT Projects using the same template files.

## Repository structure
```
MedicalDialog/
├── README.md
├── LICENSE
├── DISCLAIMER.md
├── templates/
│   ├── medical_summary.md  ← short personal medical history
│   ├── medications.md      ← current medications & supplements
│   ├── labs.csv            ← labs results
│   ├── imaging_and_procedures.md  ← imaging and procedure reports (X-ray, MRI results, colonoscopy, pathology reports, etc.)
│   └── AI_instructions     ← instructions to AI system
├── file_examples/
│   ├── medical_summary.md  ← short personal medical history
│   ├── medications.md      ← current medications & supplements
│   ├── labs.csv            ← labs results
│   ├── imaging_and_procedures.md  ← imaging and procudere reports (imaging like X-ray, MRI results, colonoscopy, pathology reports, etc.)
│   └── AI_instructions     ← instructions to Claude project, ChatGPT project or Gemini gem.
├── dialog_examples/
│   ├── dialog1.md  ← example of a dialog
│   ├── dialog2.md  ← example of a dialog
│   └── dialog3.md  ← example of a dialog
├── updates_examples/
│   ├── medications_update.md  ← update of medications
│   ├── labs_update.md  ← updates of labs results
│   ├── new_labs.pdf    ← new labs results in a pdf format
│   ├── imaging_and_procedures_update.md  ← update of imaging and procedures
│   └── new_xray.pdf  ← new imaging result in a pdf format
└── setup/
    ├── claude_projects.md
    ├── gemini_gems.md
    └── chatgpt_projects.md
```
	
## Getting started

	* Copy the template/ files and fill them in with your own health information. Follow examples in file_examples.
	* Follow the setup guide for your AI platform of choice in setup/
	* To understand how to interact with the system, try the example queries in dialog_examples
	* Interact with the system before or after doctor appointment, when you get new medical informaation or when you have medical questions.

## Status

Work in progress. Templates and setup guides coming soon. Contributions welcome.

## License

MIT License. See LICENSE for details.
