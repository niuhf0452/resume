# Resume Project

## CSS/HTML Design Principles

- **Use em units for sizing.** This unifies screen and print rendering, minimizing the need for `@media print` overrides. The base `font-size` is set on `body`; all other sizes are relative to it.

- **Flatten block nesting for better print pagination.** Keep each line or paragraph as its own block element. Avoid wrapping multiple items in a container div. The browser's automatic page-break works best when it can break between any two small blocks, rather than being forced to keep large nested blocks together.

- **Inherit font and color by default.** Only set `font-size` on elements with browser defaults that need overriding (h1, h2, h3, li). All other elements (`.meta`, `.light`, `.desc`, etc.) should inherit from their parent.

- **Prioritize layout over semantics in HTML structure.** Semantically, sections should be wrapped in nested blocks, but this prevents the browser's auto-pagination from working well. We deliberately flatten the structure into individual lines/paragraphs to get better print page breaks. This is a conscious trade-off.
