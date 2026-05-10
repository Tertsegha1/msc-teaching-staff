# MSc CS&T Teaching Staff Directory — Blackboard Ultra
**Ulster University QAHE · MSc Computer Science & Technology**

Pure HTML/CSS staff bio pages designed to be copied and pasted directly into Blackboard Ultra text blocks. No external hosting, no servers, no admin access required — everything lives inside Blackboard.

---

## 📁 Files in This Repo

All files are inside the `blackboard-pages/` folder.

| File | Blackboard Location |
|------|-------------------|
| `00-programme-all-staff.html` | Programme Support area |
| `01-CMP701-digital-transformation.html` | CMP701 module page |
| `02-COM745-big-data.html` | COM745 module page |
| `03-COM747-data-science.html` | COM747 module page |
| `04-COM759-knowledge-engineering.html` | COM759 module page |
| `05-COM762-deep-learning.html` | COM762 module page |
| `06-COM769-scalable-software.html` | COM769 module page |
| `07-BUS701-business-analysis.html` | BUS701 module page |
| `08-BMG921-strategy.html` | BMG921 module page |

---

## 🚀 How to Add a Page to Blackboard Ultra

**Do this once for each of the 9 pages:**

### Step 1 — Open the file
Click the file name above → click **Raw** (top right of the file view) → Select All (`Ctrl+A`) → Copy (`Ctrl+C`).

### Step 2 — Go to the Blackboard module page
Open the relevant module or programme support area in Blackboard Ultra.

### Step 3 — Add a Text content block
Click **+** to add content → choose **Text**.

### Step 4 — Open the HTML source editor
In the text editor toolbar, click the **`< >`** button (HTML source / code view).

### Step 5 — Paste and save
Delete any existing content in the source editor → Paste (`Ctrl+V`) → click **Save** or **Done**.

The staff bio page will appear immediately on the Blackboard page.

> **Tip:** Give the content block a title like *"Teaching Staff"* so students can find it easily in the page outline.

---

## ✏️ Adding a New Staff Bio

When a staff member's bio form is received, follow these steps:

### Step 1 — Copy the card template
Open the relevant module page file (e.g. `02-COM745-big-data.html`) in any text editor (Notepad is fine). Find the comment that says:

```
<!-- ═══ PASTE STAFF CARDS HERE WHEN BIOS ARE RECEIVED ═══ -->
```

Paste the following block **above** that comment and fill in the details:

```html
<div class="bbs-card">
  <div class="bbs-card-top">
    <div class="bbs-av">XX</div>  <!-- Replace XX with the person's initials -->
    <div class="bbs-cn">
      <h3>Dr. Full Name Here</h3>
      <div class="bbs-role">Senior Lecturer</div>
    </div>
  </div>
  <div class="bbs-card-body">
    <div class="bbs-quals">
      <span class="bbs-qual">PhD</span>
      <span class="bbs-qual">FHEA</span>
      <!-- Add or remove qualification badges as needed -->
    </div>
    <div class="bbs-mods">
      <span class="bbs-mod">COM745</span>
      <!-- Add more module badges if they teach multiple modules -->
    </div>
    <div class="bbs-bio">Paste the full bio text here...</div>
    <hr class="bbs-divider">
    <span class="bbs-rlbl">Research &amp; Expertise</span>
    <div class="bbs-research">List research interests and expertise here...</div>
    <a class="bbs-email" href="mailto:email@ulster.ac.uk">&#9993; email@ulster.ac.uk</a>
    <div class="bbs-office">📍 Office location · 🕐 Office hours</div>
  </div>
</div>
```

### Step 2 — Remove the empty state (if present)
If the page currently shows the "Staff profiles coming soon" message, delete the entire block between these two comments:

```
<!-- ═══ PASTE STAFF CARDS HERE WHEN BIOS ARE RECEIVED ═══ -->
```
...and...
```
</div>  <!-- end bbs-grid -->
```

Replace it with your new card and the closing `</div>` tag.

### Step 3 — Update the staff count
In the `<span class="bbs-count">` tag near the top of the file, update the number (e.g. `2 staff members`). **Delete this span entirely** if you prefer not to show a count.

### Step 4 — Re-paste into Blackboard
Open the file → select all → copy → go to the Blackboard page → edit the Text block → open HTML source → select all → paste → save.

> If a staff member teaches **multiple modules**, add their card to each relevant module page file and to `00-programme-all-staff.html`.

---

## 📸 Adding a Profile Photo

By default, cards show the staff member's initials in a coloured circle. To add a photo:

**Step 1** — Get a headshot photo (JPEG or PNG, ideally square)

**Step 2** — Convert it to base64 using one of these free tools:
- [www.base64-image.de](https://www.base64-image.de)
- [base64.guru/converter/encode/image](https://base64.guru/converter/encode/image)

**Step 3** — In the card HTML, replace the initials `<div>` with an image `<div>`:

Replace:
```html
<div class="bbs-av">TA</div>
```
With:
```html
<div class="bbs-av"><img src="data:image/jpeg;base64,PASTE_BASE64_STRING_HERE" alt="Dr. Name"></div>
```

---

## 📋 Blackboard Survey — Collecting Bios from Staff

Set up a **Survey** in Blackboard Ultra (Create → Survey) with the following questions. Once staff submit, you paste their responses into the relevant HTML files.

| # | Question | Type |
|---|----------|------|
| 1 | Full name as you want it displayed (include your title, e.g. Dr., Prof.) | Short answer |
| 2 | Title / Position (e.g. Senior Lecturer, Visiting Lecturer) | Short answer |
| 3 | Qualifications to display (e.g. PhD, FHEA, MBCS — tick all that apply) | Multiple select |
| 4 | Ulster University / QAHE email address | Short answer |
| 5 | Which modules do you teach? (tick all that apply) | Multiple select — list all 8 module codes |
| 6 | Professional Bio — write in the **third person** (e.g. "Dr. Smith is…"), 2–3 paragraphs | Essay / Long answer |
| 7 | Research Interests & Areas of Expertise | Long answer |
| 8 | Office / Room location | Short answer |
| 9 | Office Hours or student availability | Short answer |
| 10 | Profile photo | File upload (JPEG or PNG) |

**Settings:** Not graded · Visible to teaching staff only · Responses visible to instructor only.

---

## 📦 Module Reference

| Code | Module Name | File |
|------|-------------|------|
| CMP701 | Digital Transformation | `01-CMP701-digital-transformation.html` |
| COM745 | Big Data and Infrastructure | `02-COM745-big-data.html` |
| COM747 | Data Science & Machine Learning | `03-COM747-data-science.html` |
| COM759 | Knowledge Engineering | `04-COM759-knowledge-engineering.html` |
| COM762 | Deep Learning & Its Application | `05-COM762-deep-learning.html` |
| COM769 | Scalable Advanced Software Solutions | `06-COM769-scalable-software.html` |
| BUS701 | Business Analysis Fundamentals | `07-BUS701-business-analysis.html` |
| BMG921 | Strategy for Business Development | `08-BMG921-strategy.html` |

---

## 👤 Staff Directory Status

| Name | Modules | Status |
|------|---------|--------|
| Dr. Tertsegha Joseph Anande | CMP701 | ✅ Live |
| COM745 staff | COM745 | ⏳ Pending |
| COM747 staff | COM747 | ⏳ Pending |
| COM759 staff | COM759 | ⏳ Pending |
| COM762 staff | COM762 | ⏳ Pending |
| COM769 staff | COM769 | ⏳ Pending |
| BUS701 staff | BUS701 | ⏳ Pending |
| BMG921 staff | BMG921 | ⏳ Pending |

*Update this table as bios are received and added.*

---

## 📞 Maintained by
**Dr. Tertsegha Joseph Anande**
Deputy Programme Leader, MSc Computer Science & Technology
Ulster University QAHE · [tertseghaanande@gmail.com](mailto:tertseghaanande@gmail.com)
