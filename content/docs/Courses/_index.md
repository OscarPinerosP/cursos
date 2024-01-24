---
# Leave the homepage title empty to use the site title
title: 'Cursos'
date: 2022-10-24
type: blog

sections:
  # A section to display blog posts
  - block: collection
    id: section-1
    content:
      title: Section 1
      subtitle: A subtitle
      text: Add any **markdown** formatted content here - text, images, videos, galleries - and even HTML code!
      # Display content from the `content/post/` folder
      filters:
        folders:
          - docs/courses/
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      # Choose your content listing view - here we use the `showcase` view
      view: showcase
      # For the Showcase view, do you want to flip alternate rows?
      flip_alt_rows: true
  - block: portfolio
    # id: courses
    content:
      title: Cursos
      filters:
        folders:
          - docs/Python
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Data Science
          tag: Data Science
        - name: Python
          tag: Python
        - name: Other
          tag: Other
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false

---

Aprende a programar en Python desde cero. En este curso te ayudaré a comprender los fundamentos y características esenciales del lenguaje de programación Python de una manera sencilla, fácil de comprender y sobre todo práctica.
