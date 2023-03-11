---
# An instance of the Pages widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: collection

# This file represents a page section.
headless: true
active: true

# Order that this section appears on the page.
weight: 25

title: Recent posts
subtitle:

url: blogs

content:
  # Page type to display. E.g. post, talk, publication...
  page_type: blog
  # Choose how many pages you would like to display (0 = all pages)
  count: 3
  # Filter on criteria
  filters:
    author: ""
    category: ""
    tag: ""
    exclude_featured: false
    exclude_future: false
    exclude_past: false
    publication_type: ""
  # Choose how many pages you would like to offset by
  offset: 0
  # Page order: descending (desc) or ascending (asc) date.
  order: desc
  archive:
    enable: true
    link: blogs

design:
  # Choose a view for the listings:
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   4 = Citation (publication only)
  view: compact
---
