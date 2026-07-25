# Proud To Smile Dentistry — Website Project Intake & Kickoff Breakdown

*Source: Project intake form + intake call with Michelle Cordero (Office Manager), Nicole Wilkinson (Regional Director of Operations), and Dr. Patty — July 15*

## Project Intake

### Business Information

**Business Name:** Proud To Smile Dentistry
**Tagline:** "A beautiful smile is the essence of health" ("We make our patients Proud To Smile")
**Industry:** Healthcare — General/Cosmetic Dentistry

### Target Audience

**Primary audience:** Local patients and families seeking general and cosmetic dental care *(suggested based on call context — confirm with client)*
**What action should visitors take?** Call the office (primary CTA); book an appointment online via ZocDoc (secondary option, confirmed on call)

### Reference Sites

**Primary reference (design/structure/layout to clone):** https://pdp.carenetic.digital/ (also reachable via https://pdp.skybox4.com/, which redirects here)
**Real business site (source of truth for actual content/business info):** https://www.proudtosmile.com/

Note: These serve different purposes. pdp.carenetic.digital is a multi-location demo site whose design, page structure, and section layout we are cloning — reskinned in Proud To Smile's own blue/green color palette instead of the reference site's colors (confirmed on call). proudtosmile.com is the real, live business we're building the new site for — its content (address, hours, providers, services, testimonials, bios) is the source of truth and overrides anything from the design reference. Provider/location page counts follow the real business (1 location, 2 providers: Dr. Patty + hygienist Karima, plus a new associate joining in August), not the reference's fabricated roster (2 locations, 18 doctors) — see `.site-factory/state.json` `pages.notes`.

### Brand Voice

**Tone:** Professional, approachable, warm/welcoming, modern and up-to-date, expert-driven (confirmed on call)
**Key messages:**
- Patients are genuinely cared for — a comfortable, warm, welcoming place to be, not a "run-of-the-mill" dental practice
- Modern, state-of-the-art dentistry
- Dr. Patty is a recognized authority — a speaker and mentor in the dental profession — patients are getting expert-level care
- A happy, close-knit staff and comfortable office atmosphere
- Comprehensive general + cosmetic dentistry services under one roof

### Content Sources

**Existing content:** https://www.proudtosmile.com/ — reuse real business info (address, phone, hours, provider bios, services, testimonials) as-is from this site, pending Michelle's review/edits (see Services Pages and About the Practice below).
**Content to generate:** Section copy/layout follows the pdp.carenetic.digital reference structure, populated with real Proud To Smile content. Do not fabricate providers, locations, testimonials, or stats beyond what's on proudtosmile.com.

### Technical Requirements

**Forms:** Dedicated patient-forms page (new patient forms, insurance update forms, etc.) built on a HIPAA-compliant JotForm setup, with submissions routed to email notifications (confirmed on call, coordinated via Kelsey)
**Integrations:** Auto-pulled Google reviews (embedded script) for testimonials; ZocDoc online booking link; social links to Facebook, Instagram, YouTube, and TikTok (all confirmed active)
**Special features:** Blog (existing content migrated at launch), a new News/Press section (magazine features, speaking engagements, new hires), a video/resource library page for short-form video content, and a before/after photo gallery (side-by-side layout, confirmed)

---

## Website Kickoff Breakdown

### Homepage

**Should have:** updated hero imagery reflecting the practice today (no new video for launch — decided to skip video and use strong static photos instead, revisit video later if footage becomes available). Tone: professional, warm/welcoming, modern, and reflective of Dr. Patty's standing as a recognized speaker/expert in the field.

**Should not have:** the current outdated intro video (features former employees); current stock photos (to be replaced with real practice photos wherever possible).

### Services Pages

**Should have:** the full, accurate current service list — cleanings, veneers, pediatric dentistry, extractions, teeth whitening, emergency dentistry, crowns, dental implants, Botox, dentures, periodontal therapy, cosmetic/restorative dentistry, oral surgery, and clear aligner therapy — with copy Michelle confirms after reviewing a scraped content doc.

**Should not have:** "Invisalign" as the on-page brand name/Q&A — finalized branding is **Clear Aligner Therapy** throughout the site. "Invisalign" is retained only in backend metadata/SEO so search traffic still finds the site; on-page copy may note the product is similar to Invisalign for recognition.

### Providers/Team Page

**Should have:** Dr. Patty and hygienist Karima (the only two currently accurate), plus the new associate starting in August (headshot/bio already with Kelsey). Consider short personal video intros (Dr. Patty's career story, new associate) alongside or instead of text bios.

**Should not have:** other staff (front desk, etc.) — page is deliberately limited to providers only, to avoid upkeep on every staff turnover. Revisit in ~1 year. Michelle also opted herself out.

### Video/Resource Content

**Should have:** a new video library/"resource library" page (blog-style cards) housing existing short-form videos (Dr. Patty explaining veneers, etc.).

### Photos (Before/After + General)

**Should have:** new office/team photos over time as Michelle's team completes photography training; keep existing before/afters that look acceptable in the meantime. **Layout finalized: side-by-side** (not hover/slider) for launch.

**Should not have:** current stock photos; any before/afters Michelle flags as bad.

### Testimonials

**Should have:** auto-pulled Google reviews (arranged via Kelsey) plus the existing video testimonials featured on the same page.

### Contact/Booking

**Should have:** phone call as the primary CTA, with online booking also promoted (Dr. Costello being connected to ZocDoc). Copy should lean "call us" while still surfacing the booking option.

### Office Info

- **Address:** confirmed correct, no change.
- **Hours:** updating effective Aug 17. **Monday finalized at 8am–6pm** (extended hours). Tue/Wed 9–6, Thu 7–4, Fri per current schedule — Michelle still owes final written confirmation of remaining days.

### Patient Portal

**Finalized: removed from the new site.** Not currently in use; not required by PDP at this time.

### Patient Forms

**Should have:** a dedicated forms/patient-info page with links to all relevant forms (new patient, insurance update, etc.), built on Kelsey's HIPAA-compliant JotForm setup, with submissions routed to email notifications.

**Open:** Michelle still needs to review the current linked form and supply any additional forms.

### Legal Pages (Privacy, Terms, HIPAA, etc.)

**Finalized: built as placeholders for now**, to be filled in once PDP corporate confirms requirements (e.g., HIPAA policy references, photo release).

### About the Practice

**Should have:** existing content as the starting point — Michelle to review and confirm accuracy/edits.

### Logos/Affiliations

**Should have:** all current logos retained; nothing flagged for removal; more can be added later if needed.

### News/Press (New Section)

**Should have:** a new section (structured like the blog) for press mentions (1 local + 2 national magazine features), speaking engagements, and new-hire announcements — reinforcing Dr. Patty's reputation as a recognized expert/mentor.

### Blog

**Should have:** all existing blog content migrated over at launch.

**Open:** ownership of ongoing monthly content post-launch still undecided — Michelle offered to pre-write a batch of 12 posts as one option.

### Social Media

**Should have:** Facebook, YouTube, Instagram, and TikTok links — all confirmed active, just need working links verified.

---

## Remaining Open Items

1. Confirm primary target audience statement with client.
2. Michelle's confirmation of full/accurate services list and page copy (pending content-scrape review).
3. Final hours for Tue–Fri beyond what's confirmed above.
4. Patient forms — which existing/additional forms to include.
5. Who creates ongoing monthly blog content after launch.
6. PDP corporate's specific legal-page requirements (to fill in the placeholders).
