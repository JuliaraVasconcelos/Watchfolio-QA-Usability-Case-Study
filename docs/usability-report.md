# 🐞 Usability & Bug Report

---

### [USAB-01] Excessive friction when updating viewing date
* **Feature / Screen:** Title Details / Status Update
* **Severity Level:** Medium
* **Description:** The interface presents 4 distinct selection options for date modification, increasing cognitive load unnecessarily. Furthermore, selecting a date within the calendar component does not confirm the action; users must tap an additional "Use" button.
* **Steps to Reproduce:**
  1. Open any title details page.
  2. Tap the pencil icon to edit viewing status.
  3. Attempt to modify the viewing date.
* **Expected vs. Actual Result:**
  * *Expected:* Direct display of the native calendar picker and single-tap date selection.
  * *Actual:* Display of 4 confusing options and double confirmation required (calendar checkmark + "Use" button).
* **Suggested Fix:** Open the native calendar component directly and apply the date change upon selection.
* **Evidence:** *![friction updating date](https://www.image2url.com/r2/default/images/1791732263673-fc0d632f-6919-4e06-8b45-dde65b4ebc4a.jpg)*

---

### [USAB-02] Automatic viewport zoom on search bar focus
* **Feature / Screen:** Profile / Create List / Search Title
* **Severity Level:** Low
* **Description:** Tapping the search bar to add a title to a new custom list causes the iOS viewport to automatically zoom in, distorting the page layout and framing.
* **Steps to Reproduce:**
  1. Navigate to the **Profile** tab.
  2. Select **Lists** -> **New List**.
  3. Enter list name and description.
  4. Tap the title search bar.
* **Expected vs. Actual Result:**
  * *Expected:* The keyboard should slide up without altering the page scale or zoom.
  * *Actual:* The screen zooms in automatically upon focusing on the input field.
* **Technical Root Cause & Fix:** In iOS WebViews and mobile safari frameworks, input fields with a `font-size` smaller than `16px` trigger an automatic system zoom. Increasing the font size of the search input field to `16px` will resolve this behavior.
* **Evidence:** *![viewport zoom](https://www.image2url.com/r2/default/images/1791732351479-6fa6aaed-2a1b-448a-8c69-51e54538d8a2.jpg)*

## 📐 Nielsen's Usability Heuristics Mapping

### [USAB-01] Date Selection Friction
* **Heuristic Violated:** **#8 Aesthetic and Minimalist Design** & **#7 Flexibility and Efficiency of Use**
* **Analysis:** Presenting 4 separate options and requiring a double-confirmation flow (calendar checkmark + "Use" button) increases cognitive load and unnecessary user interactions. Streamlining to a single native calendar picker directly supports efficient task completion.

---

### [USAB-02] Automatic Viewport Zoom
* **Heuristic Violated:** **#4 Consistency and Standards**
* **Analysis:** Unintended viewport zooming upon text field focus violates standard iOS interface guidelines. Maintaining system-wide layout consistency prevents user confusion and layout distortion.
