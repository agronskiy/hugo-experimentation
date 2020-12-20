---
---

# With blank line before comment

Shortcode `% inneronly %`:

{{% inneronly %}}
```golang
func f() {

    // comment
}
```
{{% /inneronly %}}

Shortcode `< inneronly >`:

{{< inneronly >}}
```golang
func f() {

    // comment
}
```
{{< /inneronly >}}

**PROBLEM**  Shortcode `% innermarkdownify %`:

{{% innermarkdownify %}}
```golang
func f() {

    // comment
}
```
{{% /innermarkdownify %}}

Shortcode `< innermarkdownify >`:

{{< innermarkdownify >}}
```golang
func f() {

    // comment
}
```
{{< /innermarkdownify >}}

**PROBLEM** Shortcode `% innermarkdownifysafehtml % `:

{{% innermarkdownifysafehtml %}}
```golang
func f() {

    // comment
}
```
{{% /innermarkdownifysafehtml %}}

Shortcode `< innermarkdownifysafehtml >`:

{{< innermarkdownifysafehtml >}}
```golang
func f() {

    // comment
}
```
{{< /innermarkdownifysafehtml >}}

# Without blank line before comment

Shortcode `% inneronly %`:

{{% inneronly %}}
```golang
func f() {
    // comment
}
```
{{% /inneronly %}}

Shortcode `< inneronly >`:

{{< inneronly >}}
```golang
func f() {
    // comment
}
```
{{< /inneronly >}}

Shortcode `% innermarkdownify %`:

{{% innermarkdownify %}}
```golang
func f() {
    // comment
}
```
{{% /innermarkdownify %}}

Shortcode `< innermarkdownify >`:

{{< innermarkdownify >}}
```golang
func f() {
    // comment
}
```
{{< /innermarkdownify >}}

Shortcode `% innermarkdownifysafehtml % `:

{{% innermarkdownifysafehtml %}}
```golang
func f() {
    // comment
}
```
{{% /innermarkdownifysafehtml %}}

Shortcode `< innermarkdownifysafehtml >`:

{{< innermarkdownifysafehtml >}}
```golang
func f() {
    // comment
}
```
{{< /innermarkdownifysafehtml >}}
