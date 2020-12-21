---
---

# Trying to render table markdown with various inline elements:

### With `% debuginner %`

{{% debuginner %}}
| header with **bold** reference[^1]|
|----|
|cell `with code` |
{{% /debuginner %}}


### With `< debuginner >`

{{< debuginner >}}
| header with **bold** reference[^1] |
|----|
|cell `with code` |
{{< /debuginner >}}

[^1]: test reference
