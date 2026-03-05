# Sympolar — Intake Form System
## Deploy Guide · sympolarllc@gmail.com

---

## FILE STRUCTURE
```
sympolar-site/
├── contact.html         ← Step 1: 30-second quick contact
├── inquiry.html         ← Step 2: Structured project inquiry
├── onboarding.html      ← Step 3: Full website build intake
├── added-touch.html     ← Step 4: Optional deep-detail form
└── css/
    └── sympolar.css     ← Shared styles (all 4 pages use this)
```

---

## HOW TO GO LIVE (Netlify — Fastest, Free)

1. Go to **https://netlify.com** → Sign up free with your Gmail
2. Click **"Add new site" → "Deploy manually"**
3. **Drag the entire `sympolar-site/` folder** into the deploy window
4. Your site is live instantly at a URL like `amazing-bear-abc123.netlify.app`
5. To connect `sympolar.com` → Site settings → Domain management → Add custom domain

Your 4 pages become:
- `sympolar.com/contact`
- `sympolar.com/inquiry`
- `sympolar.com/onboarding`
- `sympolar.com/added-touch`

---

## HOW FORM SUBMISSIONS WORK

All 4 forms use **mailto:** — when a client submits, their email client opens with a pre-filled, formatted email ready to send to `sympolarllc@gmail.com`.

**What you receive:** A clean, structured email with all the client's answers organized by section.

**Subject lines auto-generated:**
- `Quick Consultation Request — Sympolar`
- `Project Inquiry — [Business Name] — Sympolar`
- `Website Onboarding — [Business Name] — Sympolar`
- `Added Touch Details — [Name] — Sympolar`

---

## UPGRADE PATH (when you're ready)

**Replace mailto with Formspree (free tier, no email client required):**

1. Go to https://formspree.io → create free account
2. Create a new form → copy your endpoint (looks like `https://formspree.io/f/xyzabc`)
3. In each HTML file, find:
   ```html
   <form id="..." onsubmit="handleSubmit(event)">
   ```
4. Change to:
   ```html
   <form action="https://formspree.io/f/YOUR_ID" method="POST">
   ```
5. Remove the `<script>` block at the bottom of each file
6. Add a `_next` hidden field to redirect after submit:
   ```html
   <input type="hidden" name="_next" value="https://sympolar.com/thank-you">
   ```

Formspree gives you: spam filtering, email notifications, submission dashboard.

---

## PIPELINE FLOW

```
Traffic lands on site
        ↓
contact.html     (30 seconds · name, email, phone, preferred contact)
        ↓
inquiry.html     (2 minutes · business basics, goal, pages, style)
        ↓
onboarding.html  (5 minutes · full build info — static site only)
        ↓
added-touch.html (optional · story, awards, testimonials, media links)
```

Each level = higher commitment = warmer lead.
**Added Touch clients are your most detail-oriented clients** — flag these for extra care.

---

## NOTES

- **No financial discussion** anywhere in onboarding or added touch
- **No bookings, shop, appointments** — basic static site pages only
- All forms submit structured, section-organized emails for easy reading
- The Added Touch form uses **dashed gold borders** to visually signal "optional depth"
- Mobile responsive on all screens

---

*Sympolar · sympolar.com · sympolarllc@gmail.com*
