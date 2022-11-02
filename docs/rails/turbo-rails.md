# Turbo rails

- [BEM methodology](https://en.bem.info/methodology/)

## Turbo Drive
- By default, Turbo Drive speeds up our Ruby on Rails applications by converting all link clicks and form submissions into AJAX requests
- Active using Turbo Drive by add
```javascript
import "@hotwired/turbo-rails"
```
- To disable Turbo Drive
```ruby
# On link
<%= link_to "New quote",
    new_quote_path,
    class: "btn btn--primary",
    data: { turbo: false } %>

# On form
<%= simple_form_for quote,
    html: {
      class: "quote form",
      data: { turbo: false }
    } do |f| %>

# On javascript
Turbo.session.drive = false
```

- Content on `<head>` can reload by adding `data-turbo-track="reload"`. On every new request, Turbo Drive compares the DOM elements with data-turbo-track="reload" in the `<head>` of the current HTML page and the `<head>` of the response. If there are differences, Turbo Drive will reload the whole page.

## Turbo Frames
- Rule 1: When clicking on a link within a Turbo Frame, Turbo expects a frame of the same id on the target page. It will then replace the Frame's content on the source page with the Frame's content on the target page.

## Reference
- https://www.hotrails.dev/turbo-rails/turbo-drive