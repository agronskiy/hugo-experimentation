## Illustration of the lookup order precedence.

Note that `content` has:
- `some-section` without `_index`
- `another-section` with `index` with `url: /some-section` (i.e. it tries to
  replace `some-section`)

Below, we play with the `list.html` template in three variations:
- Normal list template
- Empty (0 byte lenght) list template
- Removed completely

### `lookup-order-section-1`

`/layouts/_default/list.html` template is present and non-empty.

`http://localhost/some-section` is generated with `list` template *even though* there is no explicit
`_index.md`. This is due to automatic rendering of section pages.


### `lookup-order-section-2`

`/layouts/_default/list.html` template is present and empty.

`http://localhost/some-section` is generated with `single` (with the source `/content/another-section`) because the `list.html` has zero length hence the section page here is not automatically rendered.

### `lookup-order-section-3`

`/layouts/_default/list.html` template is removed.

`http://localhost/some-section` is generated with `single` (with the source `/content/another-section`) but there is build warning:
```
➙  hugo serve

Start building sites …
WARN 2020/12/02 07:28:38 found no layout file for "HTML" for kind "section": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
```
