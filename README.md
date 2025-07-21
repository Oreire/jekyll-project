To integrate your `project-card.html` and accompanying CSS into a Jekyll-based site effectively, here’s the ideal folder placement:

---

### 📁 The Recommended Folder Structure

```
your-jekyll-site/
├── _includes/
│   └── project-card.html          ← Reusable component lives here
├── assets/
│   └── css/
│       └── project-card.css       ← Styles specific to your card layout
├── _layouts/
│   └── default.html               ← Reference the CSS file here
├── projects.md                    ← Page that includes the component
├── _config.yml
├── index.md or index.html
└── ... other site files
```

---

### 🔗 How to Link the CSS in `_layouts/default.html` or your base layout

Add this line inside the `<head>` section:

```html
<link rel="stylesheet" href="{{ '/assets/css/project-card.css' | relative_url }}">
```

This ensures your card styling is available site-wide or on any page that uses the layout.

---

### 📥 How to Include Cards in `projects.md`

```liquid
{% include project-card.html
  title="IAM Governance via Terraform"
  description="Codified least-privilege access policies with modular Terraform. Enhanced auditability and cloud security posture."
  link="https://github.com/yourusername/terraform-iam-governance"
  docs="https://yourusername.github.io/terraform-iam-governance"
  tags="['Terraform', 'Security', 'IAM']"
%}
```

---

Would you like me to help you convert all your existing project entries into this reusable format, or scaffold a dynamic grid-style layout for your homepage? You're just a few tweaks away from turning this into a sleek, modern portfolio.
