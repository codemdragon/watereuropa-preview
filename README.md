# Water Europa Website Project Plan

This README documents the required client information and decision points needed before the project moves into final design and development.

## Project Summary

The project is a Water Europa website built using HTML, CSS, and JavaScript. It will include a responsive landing page, project storytelling, founder story, RO plant case study, future expansion details, donation/contact sections, and a content-editable admin panel.

The project is intended to be lightweight and editable without a traditional database backend. Content will be managed through GitHub API and a `db.json` file, with a simple admin interface for content updates.

## Google Stitch UI Plan

Use Google Stitch to create a fast first-pass visual concept for the public website, then carry the chosen visual language into the admin panel. Treat this as a UI exploration: the brand colors and final copy are not approved yet.

### Confirmed direction

- **Public brand:** Water Europa. The logo file is `Logo.png`; use it if available in Stitch, otherwise use a simple logo placeholder.
- **Tone:** Clear, credible, and formal enough for a university application, while still human and community-focused. Explain what Water Europa does directly in the hero.
- **Visual identity:** Explore a small set of color directions before choosing one. A water-inspired blue/teal palette with warm neutral backgrounds is a reasonable starting concept, not a final brand decision.
- **Primary navigation/content:** Home, Our Story, Kashmore Project, Future Plans, and Donate/Contact. Start with a single responsive landing-page concept using clear navigation to these sections.
- **Impact facts:** More than 300 people served daily and over $10,000 raised. Keep these figures prominent but avoid inventing additional statistics.
- **Project story:** The Kashmore RO plant has operated since July 2024. Include space for community, plant/machinery, and treatment-process photos; exact capacity and daily access figures still need client confirmation.
- **Future plans:** Kandhkot is planned for early 2027, followed by Shikarpur and Ghotki in late 2027. Present these as plans, not completed projects.
- **Donation interaction:** Show preset donation amount choices and a clear WhatsApp CTA. The CTA will open a configurable, pre-filled message; it is a contact handoff, not online payment processing. The WhatsApp number and exact amounts/message remain configurable or to be confirmed.
- **Admin panel:** Keep it straightforward for one primary client user. It should fit the public site's visual language and support editing content, images, contact details, location, social links, and the floating social button's enable/disable setting.

### Stitch generation sequence

1. Generate the responsive public landing page first, prioritizing the hero, impact, project story, future plans, and donation/contact sections.
2. Explore a few restrained palette treatments for the same layout; choose the brand direction with the client before treating any colors as final.
3. Once the public concept is selected, generate a simple admin dashboard and content-editing screen using the same typography, colors, and components.
4. Use placeholders for missing founder names, final copy, project photos, contact details, donation amounts, and confirmed plant capacity. Do not fabricate these details.

### Initial Stitch prompt

```text
Create a polished, responsive desktop-first landing page concept for Water Europa, a student-led humanitarian project bringing access to safe drinking water to underserved communities. The site must clearly explain its purpose in the first screen and feel credible and formal for a university application while remaining warm, human, and community-centered. Use an editorial NGO storytelling layout, generous whitespace, accessible contrast, clear typography, and authentic documentary-style image placeholders. Explore a restrained water-inspired blue/teal palette with warm neutral backgrounds as a concept only; brand colors are not final. Use the supplied Logo.png if available, otherwise a logo placeholder.

Structure: (1) clean header with logo and navigation for Home, Our Story, Kashmore Project, Future Plans, and Donate/Contact; (2) hero with a direct safe-water mission headline, brief explanation, large project/community photo, and “Learn about our work” and “Support us” calls to action; (3) impact band featuring “300+ people served every day” and “$10K+ raised”; (4) clear explanation of poor groundwater quality, salinity/contamination, and difficulty accessing safe water, with photo space; (5) origin story with placeholders for two founders and a co-founder; (6) Kashmore project story, running since July 2024, with plant, community, and treatment-process photo placeholders and editable placeholders for capacity/access figures; (7) future-project timeline showing Kandhkot planned for early 2027 and Shikarpur/Ghotki planned for late 2027; (8) donation/contact section with preset amount buttons and a WhatsApp CTA labeled as a request/contact step, not an online payment button; (9) simple footer with contact and social link placeholders.

Use only the supplied facts. Mark unknown names, final copy, figures, photos, contact details, WhatsApp number, and donation amounts as editable placeholders. Do not imply future projects are complete, invent payment processing, or add unsupported claims. Ensure a clear mobile layout with accessible buttons and navigation.
```

## Required Client Questions

### 1. Brand & Identity
- What is the exact name and brand style to use for the website?
- Do you already have a logo file and brand colors?
Logo.png, Brand colors are to be decided, I'll give user options from figma template prolly or google stitch design for a basic concept

- Should the website use a more formal NGO-style look or a more modern humanitarian campaign look?
Its run by a student and needs it for Uni Apps so assumably formal, he said "Just handle it". It should explain it very well and it should be clear what it is directly from hero section. 

- Which founder names should be mentioned, and how should they be positioned?


### 2. Project Content
- Can you share the complete text for each section of the homepage and the project pages?
- Do you have final photos for the plant, treatment process, affected community, and founder/story sections?
- Are there any approved captions, statistics, or numbers that must be included exactly?
- Should the site include a specific tagline, mission statement, or call-to-action text?

### 3. Pages & Structure
- Are the following pages required: Home, About, Kashmore Project, Future Plans, Donate, Contact?
- Do you want an additional “Impact” section or a dedicated story page?
- Should the donation page include a direct payment button, a form, or just a contact/donation guide?
Directly redirects user to whatsapp with a preset message thats configurable from the admin panel and so is the whatsapp number or whatever their chosen social media is

- Do you want a floating social media icon that can be enabled or disabled from the admin panel?
YES

### 4. Donation & Payment Setup
- Is a donation/payment gateway required, and if yes, which provider is preferred?
- Is this gateway confirmed, or is it still under discussion?
- Should the donation button redirect to WhatsApp, a donation form, or a payment platform?
- Are there any payment processing rules, country limits, or compliance requirements?

### 5. Contact & Social Links
- What is the final email address for contact inquiries?
- What is the official WhatsApp number to include?
- Which social media platform should be linked in the floating icon?
- Do you want all social/contact links to appear in the header, footer, and floating button?

### 6. Admin Panel Access
- Who will manage the content after launch?
- Will the admin panel need full editing access for pages, contact info, images, and social links?
Again its for a student whos applying tom uni and whats it on his page, he should be the only one with access really and there should be no complications. It should be extremely straight forward to use.

- Which GitHub account should be used for the content file and deployment setup? His one, it'll be on mine till set up on his, for trasnfer ease user has to enter in their own github for config since it'll connect to his repo
- Do you want a login protected admin panel or an open editing interface for trusted staff? Only github token and basic auth is needed. No Database aside from db.json

### 7. Domain & Deployment
- Which domain should be used for the final website?
- Is the domain `watereuropa.org` confirmed? yes, will be setup using porksbun and vercel 
- Do you already have access to the Porkbun account for setup and DNS management? he will be making a subaccount, ive had him verify already, domain matters will be settled after website built 
- Should the site be deployed on Vercel, and who will handle the Vercel account access? its gonna be on vercel, he will be given full ownership to manage it later on, so its fine for me to be admin for now
- Does the Developer need to be added as a sub-account to the Porkbun account? Yes I will be added to the subaccount 

### 8. Legal & Business Details
- What is the exact legal name of the client/organization? Project Europa
- What are the official contact details for sign-off and invoicing? Will be added via admin panel. 
- Is the developer expected to be added to the domain provider account for setup and management? Yes I will manage dns shenanigans 
- Has the client approved the pricing and maintenance terms for one-time setup and annual maintenance? we discussing stuff, signing off tmr

## Required Client Decision Checklist

Before launch, confirm the following:

- [ ] Final project name and branding
- [ ] Final content for all main sections
- [ ] Final project images and founder photos
- [ ] Approved donation/payment approach
- [ ] Final contact details and social links
- [ ] Porkbun + Vercel access info
- [ ] GitHub access for deployment/content updates
- [ ] Admin panel editing requirements
- [ ] Contract signature and payment plan

## Next Step

Use the Initial Stitch prompt above to create an exploratory public-site concept now, with placeholders for unconfirmed content and assets. Confirm the visual direction and remaining client decisions before finalizing the UI, then carry the approved design into the admin panel, deployment configuration, and launch preparation.
