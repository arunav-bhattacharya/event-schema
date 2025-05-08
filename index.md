---
title: Home
layout: home
---

# Billpay Event Schema

Below is the schema definition for Billpay events:

<div class="schema-viewer" id="schema-viewer"></div>

<script src="https://cdn.jsdelivr.net/npm/@json-editor/json-editor@latest/dist/jsoneditor.min.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
  fetch('/event-schemas/v1/BillpayEvents.json')
    .then(response => response.json())
    .then(schema => {
      const container = document.getElementById('schema-viewer');
      const options = {
        schema: schema,
        disable_edit_json: true,
        disable_properties: true,
        disable_collapse: false,
        show_errors: "never",
        no_additional_properties: true,
        theme: 'bootstrap4'
      };
      const editor = new JSONEditor(container, options);
    });
});
</script>

<style>
.schema-viewer {
  min-height: 500px;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 10px;
  margin: 20px 0;
}
</style>

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
