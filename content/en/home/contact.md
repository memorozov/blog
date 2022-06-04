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
  email: laumynkva@gmail.com
  phone: +7 999 888 77 66
  address:
    street: Kuznetsky Most Street
    city: Moscow
    region: Moscow
    postcode: '107031'
    country: Russia
    country_code: RU
  coordinates:
    latitude: '0'
    longitude: '0'
  directions: RUDN Engineering Academy Building
  office_hours:
    - '00:00 to 24:00'
  contact_links:
    - icon: github
      icon_pack: fab
      name: Github
      link: 'https://github.com/memorozov'

design:
  columns: '2'
---
