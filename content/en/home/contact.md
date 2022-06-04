---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
  email: rudn-website@danya02.ru
  contact_links:
    - icon: orcid
      icon_pack: fab
      name: ORCID
      link: 'https://orcid.org/0000-0002-2337-1176'
    - icon: x
      icon_pack: fas
      name: arXiv
      link: 'https://arxiv.org/a/0000-0002-2337-1176.html'
    - icon: github
      icon_pack: fab
      name: GitHub
      link: 'https://github.com/danya02'
    - icon: steam-square
      icon_pack: fab
      name: Steam
      link: 'https://steamcommunity.com/profiles/76561198408196875/'
    - icon: globe
      icon_pack: fas
      name: Website
      link: 'https://danya02.ru'
      

design:
  columns: '2'
---
