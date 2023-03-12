---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contacto
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
  email: nzriquelme@uc.cl
  phone: 9 34668437
  address:
    street: Eyzaguirre 1140
    city: Santiago
    region: Región Metropolitana de Santiago
    country: Chile
    country_code: CL
  Horario de oficina:
    - 'Lunes a Viernes 10:00 to 17:00'
    - 'Sábado 09:00 to 13:00'
  Coordinación de reuniones: 'https://calendly.com/nataliariquelme'
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: Envía un DM
      link: 'https://twitter.com/natyriquelmes'

design:
  columns: '2'
---
