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

# UPD after research

See https://discourse.gohugo.io/t/spurious-behavior-code-highlighter-renders-bare-html-based-on-content-and-percent-angle-bracket-shortcode/30110

It seems that no bug is here, but rather a consequence of double-markdown rendering.

Shortcode `% innermarkdownify %`, and some line with two spaces indent:

{{% innermarkdownify %}}
```plain
xxx

  // *some italic text with 2 indent*
```
{{% /innermarkdownify %}}

Shortcode `% innermarkdownify %`, and some line with three spaces indent:

{{% innermarkdownify %}}
```plain
xxx

   // *some italic text with 3 indent*
```
{{% /innermarkdownify %}}

Shortcode `% innermarkdownify %`, and some line with four spaces indent:

{{% innermarkdownify %}}
```plain
xxx

    // *some non-italic verbose text because of 4 indent and re-markdowning*
```
{{% /innermarkdownify %}}
