---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  # ── HOME / BIO ───────────────────────────────────────────────────────────
  # `resume-biography` shows photo, name, role, bio and links only.
  # (`resume-biography-3` also renders Education + Interests, which would
  #  duplicate the Education timeline in the section below.)
  - block: resume-biography
    id: about
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      # Leave empty to use the `bio` field from data/authors/me.yaml.
      # NOTE: text here REPLACES the bio, it does not append to it.
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded

  # ── INTERESTS ────────────────────────────────────────────────────────────
  - block: markdown
    id: interests
    content:
      title: '🔬 Interests'
      subtitle: ''
      text: |-
        - AI/ML Engineering
        - Data Science
        - Machine Learning & Deep Learning
        - Natural Language Processing
        - Quantitative Finance
        - Statistical Modelling & Simulation
    design:
      columns: '1'

  # ── EXPERIENCE (+ EDUCATION TIMELINE) ────────────────────────────────────
  - block: resume-experience
    id: experience
    content:
      username: me
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false

  # ── PROJECTS ─────────────────────────────────────────────────────────────
  # Filterable grid. Each button's `tag` must match a tag in a project's
  # front matter exactly. `tag: '*'` means "show everything".
  - block: portfolio
    id: projects
    content:
      title: Projects
      subtitle: ''
      filters:
        folders:
          - projects
      # Set to 0 to show all projects
      count: 0
      default_button_index: 0
      buttons:
        - name: All
          tag: '*'
        - name: Machine Learning
          tag: Machine Learning
        - name: Quantitative Finance
          tag: Quantitative Finance
        - name: NLP
          tag: NLP
        - name: Statistics
          tag: Statistics
        - name: Numerical Methods
          tag: Numerical Methods
    design:
      columns: 2

  # ── SKILLS ───────────────────────────────────────────────────────────────
  - block: resume-skills
    id: skills
    content:
      title: Skills
      username: me

  # ── CERTIFICATIONS ───────────────────────────────────────────────────────
  - block: resume-awards
    id: certifications
    content:
      title: Certifications
      username: me

  # ── COURSEWORK ───────────────────────────────────────────────────────────
  - block: markdown
    id: coursework
    content:
      title: '🎓 Relevant Coursework'
      subtitle: ''
      text: |-
        **Computer Science** — Machine Learning, Computational Cognitive Science, Data Structures and Algorithms

        **Statistics** — Time Series Analysis, Stochastic Processes, Probability Theory, Statistical Inference, Statistical Simulation and Data Analysis, Sampling Theory

        **Mathematics** — Computational Financial Mathematics, ANN/ML Approach for Differential Equations, Linear Algebra, Real Analysis, Several Variable Calculus, Differential Geometry, Numerical Analysis
    design:
      columns: '1'

  # ── ACHIEVEMENTS ─────────────────────────────────────────────────────────
  - block: markdown
    id: achievements
    content:
      title: '🏅 Achievements & Scholarships'
      subtitle: ''
      text: |-
        - Received the **National Talent Search Examination (NTSE) Scholarship** from the Government of India
        - Received the **INSPIRE Scholarship for Higher Education (SHE)** from the Government of India
    design:
      columns: '1'

  # ── CONTACT ──────────────────────────────────────────────────────────────
  - block: contact-info
    id: contact
    content:
      title: Contact
      username: me
      email: porush.yadav@gmail.com
      show_form: false
---
