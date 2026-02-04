# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

✅ This proof must be visible in your browser screenshot submission.

---
## Footer Deployment Date (Dynamic Implementation)

The website footer displays the deployment date dynamically to reflect the most recent deployment.
This was implemented using JavaScript to automatically generate and display the current date when the page loads.

Implementation Details

A placeholder 
```html
<span> element is added to the footer, and JavaScript injects the current date at runtime.
<span id="deployDate"></span>

<script>
  const d = new Date();
  const formattedDate = d.toISOString().split('T')[0];
  document.getElementById("deployDate").textContent = formattedDate;
</script>
```
## Explanation

The script retrieves the current system date at page load time.

The date is formatted in YYYY-MM-DD format using ISO standards.

This approach ensures the deployment date is always accurate without requiring manual updates during future deployments.