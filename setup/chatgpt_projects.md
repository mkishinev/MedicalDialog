# Setup Instructions for ChatGPT Project

*(Nick’s Medical Dialogues)*

## Create the Project

1. Open ChatGPT in your browser.
2. In the left sidebar, under **Projects** click **+ New Project**.
3. **Project Name:** `Nick's Medical Dialogues`

---

## Apply the Project Instructions

1. Click on the `Nick's Medical Dialogues` will bring Project settings window.
2. Copy the entire content of your `instructions.md` file and paste it into the **Instructions** field. 
3. Review the pasted content:

   * Replace every instance of `[PATIENT_NAME]` in the **ROLE** section with `Nick`.
4. Save the instructions.

**Important:**
The editor window may truncate visually — scroll to ensure the full content was pasted correctly.

---

## Upload the Source of Truth (Project Knowledge Files)

1. Inside the `Nick's Medical Dialogues` Project, click on **Sources**.
2. Upload the following files exactly as named:

   * `medical_summary.md`
   * `imaging_and_procedures.md`
   * `medications_and_treatments.md`
   * `labs.csv`
3. Confirm all files appear successfully attached.

---

## Finalize and Test

1. Inside the chat field within `Nick's Medical Dialogues` Project 
   ask test questions about the patient (e.g., medications, labs, history). See dialogues/dialog1 as an example.
3. Validate:

   * Correct retrieval from uploaded files
   * Proper adherence to instructions
   * Consistent formatting and reasoning

---

## Updating the Project (Ongoing Maintenance)

### A. Updating Knowledge Files (Routine Updates)

When new medical data is available:

1. Update your local files:

   * Append to `labs.csv`
   * Add new entries to `imaging_and_procedures.md`
   * Update medications or summaries as needed
2. In the Project:

   * Remove outdated file(s)
   * Upload updated versions (same filenames)
3. Continue using the Project — new chats will reflect updates.

---

### B. Updating Instructions

If you want to refine behavior or logic:

1. Open **Project Instructions**
2. Edit the content directly
3. Save changes

---

## 6. Naming Conversations

Chats within a project appear in the project's conversation list. To make individual sessions easier to navigate you may add dates to the chat names:

1. Hover over the chat in the sidebar.
2. Click the **···** (three-dot) menu that appears.
3. Select **Rename**.
4. Prefix the name with a date, e.g.:  
   *Lipid Therapy Intensification* → **2026-04-14: Lipid Therapy Intensification**
