# MSc CS&T Teaching Staff Directory
**Ulster University QAHE — MSc Computer Science & Technology**

A self-contained, single-file teaching staff bio directory designed to be uploaded directly to **Blackboard Ultra**. No external servers, no logins, no maintenance — just upload the file and paste an iframe wherever you need it.

---

## 📁 File in This Repo

| File | Purpose |
|------|---------|
| `staff-bios-bb.html` | The complete staff directory — handles both the full programme view and individual module views from a single file |

---

## 🚀 Getting Started — Upload to Blackboard

### Step 1 — Download the file
Click `staff-bios-bb.html` above → click the **Download** button (or Raw → Save As).

### Step 2 — Upload to Blackboard Content Collection
1. Log in to **Blackboard Ultra**
2. Go to **Administrator Panel** → **Content Collection**
3. Navigate to your institution or course folder (e.g. create a folder called `programme-assets`)
4. Click **Upload** and select `staff-bios-bb.html`
5. Once uploaded, **right-click the file → Copy Link** — save this URL, you will need it for every embed

> The URL will look something like:
> `https://[your-institution].blackboard.com/bbcswebdav/pid-xxx/staff-bios-bb.html`

---

## 📌 Embedding on Blackboard Pages

On each Blackboard page, add a **Text** content block → click the **`< >`** (HTML source) button in the editor → paste the relevant code below → Save.

---

### Programme Support Area — All Staff
Shows every staff member on the programme in one directory.

```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html"
  width="100%"
  height="820"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### CMP701 — Digital Transformation
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#CMP701"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### COM745 — Big Data and Infrastructure
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#COM745"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### COM747 — Data Science & Machine Learning
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#COM747"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### COM759 — Knowledge Engineering
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#COM759"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### COM762 — Deep Learning & Its Application
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#COM762"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### COM769 — Scalable Advanced Software Solutions
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#COM769"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### BUS701 — Business Analysis Fundamentals
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#BUS701"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

---

### BMG921 — Strategy for Business Development
```html
<iframe
  src="YOUR_CONTENT_COLLECTION_URL/staff-bios-bb.html#BMG921"
  width="100%"
  height="750"
  frameborder="0"
  style="border:none;border-radius:8px">
</iframe>
```

> **How does one file serve all pages?**
> The `#CMP701` part at the end of the URL is a hash — the file reads it and automatically shows only the staff for that module. Without a hash, it shows everyone.

---

## ✏️ Adding or Updating Staff Bios

All staff data lives inside a clearly marked section near the top of `staff-bios-bb.html`. Open the file in **Notepad** (or any text editor) and find:

```
// ═══════════════════════════════════════════════════════════════════════════
//  STAFF DATA — ADD OR UPDATE BIOS IN THIS SECTION ONLY
// ═══════════════════════════════════════════════════════════════════════════
```

### Adding a new staff member

Copy the template block below and paste it inside the `STAFF = [` array, filling in all fields:

```javascript
{
  name:        "Dr. Jane Smith",
  title:       "Senior Lecturer",
  email:       "j.smith@ulster.ac.uk",
  modules:     ["COM745", "COM747"],   // All modules this person teaches
  bio:         "Dr. Jane Smith is a Senior Lecturer at Ulster University QAHE with expertise in big data systems and cloud infrastructure. She holds a PhD in Computer Science from the University of Manchester and brings over 12 years of combined academic and industry experience to the programme...",
  research:    "Big Data Analytics, Cloud Computing, Distributed Systems, Data Engineering",
  office:      "Block B, Room 214",
  officeHours: "Mondays 2–4 pm, or by appointment",
  photo:       ""   // See photo instructions below
},
```

### Updating an existing staff member

Find their entry by name, edit any fields, save the file, and re-upload it to Blackboard Content Collection (overwrite the existing file). The page updates immediately.

### Removing a staff member

Delete their entire `{ ... },` block from the `STAFF` array, save, and re-upload.

---

## 📸 Adding a Profile Photo

Photos are embedded directly inside the HTML file as base64-encoded strings — no separate image files needed.

**Step 1** — Collect the staff member's photo (JPEG or PNG, ideally a square headshot)

**Step 2** — Convert to base64 using any of these free tools:
- [www.base64-image.de](https://www.base64-image.de)
- [base64.guru/converter/encode/image](https://base64.guru/converter/encode/image)

**Step 3** — Copy the full base64 string (it starts with `data:image/jpeg;base64,...`)

**Step 4** — Paste it into the `photo:` field for that staff member:

```javascript
photo: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAA..."
```

> If the `photo` field is left empty (`""`), the card will automatically display the staff member's initials in a coloured circle instead.

---

## 📋 Collecting Bios from Staff — Blackboard Survey Setup

Set up a survey in Blackboard Ultra (**Create → Survey**) using the following questions. Staff complete the form, you receive their responses, then paste them into the HTML file.

| # | Question | Field Type |
|---|----------|-----------|
| 1 | Full name (as you want it displayed to students — include your title) | Short answer |
| 2 | Title / Position (e.g. Senior Lecturer, Visiting Lecturer, Module Tutor) | Short answer |
| 3 | Ulster University / QAHE email address | Short answer |
| 4 | Which modules do you teach on this programme? (tick all that apply) | Multiple choice — options: CMP701 Digital Transformation / COM745 Big Data and Infrastructure / COM747 Data Science & Machine Learning / COM759 Knowledge Engineering / COM762 Deep Learning & Its Application / COM769 Scalable Advanced Software Solutions / BUS701 Business Analysis Fundamentals / BMG921 Strategy for Business Development |
| 5 | Professional Bio — write in the third person (e.g. "Dr. Smith is…"), 2–3 paragraphs covering your background, qualifications, experience, and what you bring to this programme | Essay / Long answer |
| 6 | Research Interests & Areas of Expertise (comma-separated list is fine) | Long answer |
| 7 | Office / Room location (leave blank if not applicable) | Short answer |
| 8 | Office Hours or availability for students | Short answer |
| 9 | Profile photo | File submission (JPEG or PNG only) |

**Survey settings:**
- Set to **not graded**
- Make available to **teaching staff only** or share as a direct link via Teams
- Set so that only **you (the administrator) can view responses**

---

## 📦 Module Catalogue Reference

| Code | Module Name |
|------|-------------|
| CMP701 | Digital Transformation |
| COM745 | Big Data and Infrastructure |
| COM747 | Data Science & Machine Learning |
| COM759 | Knowledge Engineering |
| COM762 | Deep Learning & Its Application |
| COM769 | Scalable Advanced Software Solutions |
| BUS701 | Business Analysis Fundamentals |
| BMG921 | Strategy for Business Development |

> **Adding a new module?** Open `staff-bios-bb.html`, find the `MODULES` object (just below the `STAFF` array), and add a new line:
> ```javascript
> "COM999": "New Module Name",
> ```

---

## 👤 Current Staff

| Name | Modules |
|------|---------|
| Dr. Tertsegha Joseph Anande | CMP701 |

*Update this table in the README whenever a new bio is added.*

---

## 📞 Maintained by

**Dr. Tertsegha Joseph Anande**
Deputy Programme Leader, MSc Computer Science & Technology
Ulster University QAHE
[tertseghaanande@gmail.com](mailto:tertseghaanande@gmail.com)
