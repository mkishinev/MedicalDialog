# Setup Instructions for ChatGPT Project

*(Nick’s Medical Dialogues)*

## 1. Create the Project

1. Open ChatGPT in your browser.
2. In the left sidebar, click **Projects**.
3. Click **+ New Project**.

---

## 2. Basic Configuration

* **Project Name:** `Nick's Medical Dialogues`
* **Description (optional):**
  `Personal Health Archivist & Clinical Navigator for Nick.`

---

## 3. Apply the Project Instructions

1. Open the **Project Instructions** panel.
2. Copy the entire content of your `instructions.md` file and paste it into the instructions field. 
3. Carefully review the pasted content:

   * Replace every instance of `[PATIENT_NAME]` in the **ROLE** section with `Nick`.
4. Save the instructions.

**Important:**
The editor window may truncate visually — scroll to ensure the full content was pasted correctly.

---

## 4. Upload the Source of Truth (Project Knowledge Files)

1. Inside the Project, locate the **Files** (or “Add files”) section.
2. Upload the following files exactly as named:

   * `medical_summary.md`
   * `imaging_and_procedures.md`
   * `medications_and_treatments.md`
   * `labs.csv`
3. Confirm all files appear successfully attached.

**Note:**

* File names must remain **exactly the same** to match references in instructions.
* These files act as the project’s **authoritative data source**.

---

## 5. Finalize and Test

1. Open a new chat **inside the Project**.
2. Ask test questions about the patient (e.g., medications, labs, history). See dialogues/dialog1 as an example.
3. Validate:

   * Correct retrieval from uploaded files
   * Proper adherence to instructions
   * Consistent formatting and reasoning

---

## 6. Updating the Project (Ongoing Maintenance)

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

## 7. Naming Convention for Chats (Date Tagging)

To keep conversations dates within the project:

Add a date to the chat's name using this pattern:

```
YYYY-MM-DD: <Topic>
```

**Example:**

```
2026-04-14: Lipid Therapy Intensification
```
