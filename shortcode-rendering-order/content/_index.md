---
---

# Trying to render table markdown with various inline elements :

### With `% debuginner %`

{{% debuginner %}}
| header with *italic* reference[^1] ones|
|----|
|cell `with code` |
{{% /debuginner %}}


### With `< debuginner >`

{{< debuginner >}}
| header with *italic* reference[^1] ones|
|----|
|cell `with code` |
{{< /debuginner >}}

[^1]: test reference

# Trying to render table markdown with various inline elements and markdownify:

### With `% debugmarkdownify %`

{{% debugmarkdownify %}}
| header with *italic* reference[^1] ones|
|----|
|cell `with code` |
{{% /debugmarkdownify %}}


### With `< debugmarkdownify >`

{{< debugmarkdownify >}}
| header with *italic* reference[^1] ones|
|----|
|cell `with code` |
{{< /debugmarkdownify >}}

[^1]: test reference
