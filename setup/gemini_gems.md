# Setup Instructions: Nick's Medical Dialogues (Gemini Gem)

To deploy Nick's Medical Dialogues configuration as a custom Gem in your Gemini account, 
follow these steps.

## 1. Create the Gem
1. Open the Gemini web application in the browser.
2. Locate the left-hand sidebar and click on **Gems**.
3. Click the **+ New Gem** button in the **My Gems** section.

## 2. Basic Configuration
1. **Name:** Enter `Nick's Medical Dialogues (NMD)`.
2. **Description:** Enter `Personal Health Archivist & Clinical Navigator for Nick.`

## 3. Apply the System Instructions
1. Copy the entire `instructions.md` file content and paste it into the **Instructions** text box.
   **Note**: The text box window is small. Scroll to check that the whole content was pasted. 
2. **Name the patient:** Manually change every instance of `[PATIENT_NAME]` in the **ROLE** section to `Nick`.

## 4. Upload the Source of Truth (Knowledge Base)
1. Locate the **Knowledge** section below the Instructions box.
2. Click **Add files** (or the Google Drive icon if your files are stored there).
3. Upload or link the following four exact files:
   * `medical_summary.md`
   * `imaging_and_procedures.md`
   * `medications_and_treatments.md`
   * `labs.csv`
4. Confirm all four files show as successfully attached to the Gem.

## 5. Finalize and Test
1. Click **Update** in the top right corner.
2. Open a new chat using your newly created **Nick's Medical Dialogues (NMD)** Gem.
3. Test Gem's knowledge about the patient. See example in dialogues/dialog1.

## 6. Updating the Gem in the Future
To maintain an accurate and up-to-date health archive, you must update the Gem whenever new medical data is generated or instructions change.

**Updating Knowledge Base Files (Routine Updates):**
When you get new lab results, procedures, or medication changes:
1. Update your local source files (e.g., append a new row to `labs.csv` or add a new study block to `imaging_and_procedures.md`) as explained in HOWTO.md.
2. Go to **Gem manager** and click on **Nick's Medical Dialogues (NMD)** to edit it.
3. Under the **Knowledge** section, remove the outdated file(s) by clicking the 'X' next to them.
4. Upload the newly updated version of the file(s). 
   *Note: Always keep the exact same filenames (e.g., `labs.csv`) so the Gem's core instructions can successfully target them.*
5. Click **Update**.

**Updating System Instructions:**
If you need to refine the AI's behavior, communication style, or protocols:
1. Go to **Gem manager** and edit the Gem.
2. Update the text directly in the **Instructions** box.
3. Click **Update**.

## 7. Use of short name (NMD)
Chats with Gems are placed in the same section of the left-hand sidebar as all other charts. 
To differentiate chats with a specific Gem, rename chats with this gem adding a short name of the gem and a date as follows.
 * Hover over the chat 
 * Right click on the vertical three dots
 * Select *Rename*
 * Change chat's name, e.g., *Lipid Therapy Intensification* into *NMD 2026-04-14: Lipid Therapy Intensification*