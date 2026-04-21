# Setup Instructions for Claude Project

To deploy Nick's Medical Dialogues configuration as a custom Claude Project, follow these steps.

## 1. Create the Project

1. Open the Claude web or desktop application.
2. In the left-hand sidebar, click **Projects**.
3. Click **+ New Project** and give it a name: `Nick's Medical Dialogues`.

## 2. Apply the Project Instructions (System Prompt)

1. Inside the project, click the project name or the **⚙ Edit** / settings icon to open project settings.
2. Locate the **Project Instructions** field (this is the system prompt applied to every conversation in the project).
3. Copy the entire contents of `instructions.md` and paste them into the **Project Instructions** box.
4. **Name the patient:** Replace every instance of `[PATIENT_NAME]` in the **ROLE** section with `Nick`.
5. Save / confirm the changes.

## 3. Upload the Knowledge Base

1. In the project settings, locate the **Project Knowledge** section.
2. Click **Add Content** (or the file upload button).
3. Upload the following four files:
   * `medical_summary.md`
   * `imaging_and_procedures.md`
   * `medications_and_treatments.md`
   * `labs.csv`
4. Confirm all four files appear in the project knowledge list.

> **Note:** Claude Projects have a context window limit shared across instructions and uploaded files. If the combined size of your knowledge base files approaches the limit, consider splitting lab data by year or archiving older entries to a separate file.

## 4. Test the Project

1. Start a new chat inside the **Nick's Medical Dialogues** project.
2. Test the project's knowledge about the patient. See example in `dialogues/dialog1`.

## 5. Updating the Project

**Updating Knowledge Base Files (Routine Updates):**  
When you receive new lab results, procedures, or medication changes:

1. Update your local source files (e.g., append a new row to `labs.csv` or add a new study block to `imaging_and_procedures.md`) as described in `HOWTO.md`.
2. Go to the project settings and open the **Project Knowledge** section.
3. Remove the outdated file by clicking the **×** or trash icon next to it.
4. Upload the newly updated version.  
   *Keep the exact same filenames (e.g., `labs.csv`) so the instructions can reference them correctly.*
5. Save the changes.

**Updating Project Instructions:**  
If you need to refine the AI's behavior, communication style, or protocols:

1. Open the project settings and go to the **Project Instructions** box.
2. Edit the text directly.
3. Save the changes. The updated instructions apply to all new conversations in the project.

## 6. Naming Conversations

Chats within a project appear in the project's conversation list. To make individual sessions easier to navigate add dates to the chat names:

1. Hover over the chat in the sidebar.
2. Click the **···** (three-dot) menu that appears.
3. Select **Rename**.
4. Prefix the name with a date, e.g.:  
   *Lipid Therapy Intensification* → **2026-04-14: Lipid Therapy Intensification**
