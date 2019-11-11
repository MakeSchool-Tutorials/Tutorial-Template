---
title: "Get started with writing tutorials!"
slug: getting-started
---

**The above title becomes the tutorials first header**, so an introduction to the tutorial page should be given here **before** any more headers are created.

# Supported syntax

## Headers

Use `#` to create new headers.

```
# This is an h1 header, use to partition page into steps
## This is an h2 sub-header
### This is an h3 sub-header
#### This is an h4 sub-header
```

Each `h1` header creates a "Mark Complete" button for content between it and next `h1` header. **_Make sure there is a full "step" of content for each `h1` header._**

## Text formatting

- Italics can be done with _underscores_. Use italics for the name of applications and introducing new concepts.
- Bold can be done with **asterisks**. Use bold for names of buttons.
- Bold-italics can be done with **_asterisks around underscores_**.
- Strikethrough can be done with ~~two tildes~~.
- Inline code references (file names, class names, function names, etc) can be made with `back-ticks`, code blocks are discussed below.

## Links

[This](https://github.com/MakeSchool-Tutorials/Tutorial-Template) creates a link. Relative links should only be used when [linking to assets in the repository](assets/ms-logo.png).

_Relative links to files in the same works on makeschool.com but the links will not do anything when clicked from ms-markdown-preview._

## Images

Images syntax is similar to links and will work with most image types (including `gif`). Images should be located in the page's `assets` folder and referenced locally. This syntax transforms into an HTML image tag.

```
![Alt text](assets/image_name.png "Title text")
```

turns into

```
<img src="assets/image_name.png" alt="Alt text" title="Title text">
```

Make sure that every image has both alt and title text defined. Both are important for SEO. Alt text is displayed when a user is has images disabled. Title text is displayed when a user hovers over the image.

![Make School logo](assets/ms-logo.png "Make School")

## Font Awesome Icons

Font Awesome icons (currently `v4.7.0`, see all of them [here](https://fontawesome.com/v4.7.0/icons/)) can used with:

```
![ms-fa](pencil)
```

which renders

![ms-fa](pencil)

Font Awesome icons ![ms-fa](font-awesome) are powerful because they can added inline.

## Other embedded assets

The renderer has overhauled the image syntax for embedding MP4 videos, YouTube videos, and PDF files.

### YouTube

The following syntax will embed a YouTube video into the tutorial. There are a few requirements:

1. The video must be embeddable (see video's settings on YouTube)
1. The video **must use the full or embedded URL syntax**.
    1. **Full URL:** this is the URL that is shown when playing a video. An example would be `https://www.youtube.com/watch?v=6rT00QXqZak`
    1. **Embed URL:** you can get this from the `Share --> Embed` link, and then grabbing the url that's in the `src`. An example would be `https://www.youtube.com/embed/9lMHxt_762E`
    1. Currently, you can **not** use the short-link that YouTube provides for sharing, such as `https://youtu.be/9lMHxt_762E`
1. The text in the brackets **MUST** be `[ms-video-youtube]`. No alt-text is required.

Either of the following:

```
![ms-video-youtube](https://www.youtube.com/watch?v=6rT00QXqZak)

![ms-video-youtube](https://www.youtube.com/embed/6rT00QXqZak)
```

turns into

![ms-video-youtube](https://www.youtube.com/watch?v=6rT00QXqZak)

### MP4/MOV

The following syntax will embed an MP4/MOV video with controls. Videos can be referenced with URLs or relative links if they are included in the repository. This works great with short screencasts made with QuickTime.

Similarly to YouTube videos, the text in the brackets **MUST** be `[ms-video]`. No alt-text is required.

```
![ms-video](assets/short-video.mov)
```

turns into

![ms-video](assets/short-video.mov)

### PDF

The following syntax will embed a PDF for viewing in-line. PDFs can be referenced with URLs or relative links if they are included in the repository.

![ms-pdf](assets/empty-slides.pdf)

Images can also be included by full URL. This should be avoided in favor of images being stored in the tutorial repository.

## Asset Naming

Any asset that lives locally in an `asset` folder should adhere to the following naming convention:

`placement_number-section-name_image-title`

break down of each part of the string:

- `placement_number`: the order in which the image appears on the chapter. For example, if this is the first image in the chapter, it should be `01`. If it's the fifth image in the chapter, it should be `05`
- `section-name`: name of the section. Can be abbreviated if the section name is long. For example, if the section name is "JS fundamentals", write `js-fundamentals`. If the section name is "Wow this is a really long title", then just write `wow-this-is`.
  - If abbreviating, use your best judgement. Try to keep it to no more than 3 words
- `image-title`: Brief descriptive title for the image. For example, if the image is of a comment box component, write `comment-box`

### Combined Example

Let's say you have an image of an illustration of DFS, and it's in the section named "Learning DFS" of chapter 4, and it's the second image in the tutorial. The image would be named the following:

`02_learning-dfs_dfs-illustrated.png`

### What Assets should follow this?

Anything living in the `asset` folder of each chapter. This includes:

- images
- videos (MP4/MOV)
- PDFs
- Anything else that lives in the `asset` folder of a chapter

## Lists

### Unordered lists

- This is an unordered list
- The space after the `-` is necessary!

### Ordered lists

1. This is an ordered list
1. With multiple items
1. Use one and let the processor count for you or the linter will get angry!
1. But don't be lazy...

### Nested lists

1. This is a nested list
    1. Use four spaces for each level
    1. More nested items

1. Formatting can get a little weird so only nest once!
    - You can even combine ordered and unordered lists when nesting
    - Just remember to use four spaces for each level

1. Such an amazing list

## Tables

We also support markdown tables!

| This is a header    | This is another header |
|:--------------------|:-----------------------|
| Sample contents     | Such table             |
| So nicely formatted | Much wow               |

## Code blocks

Always use fenced code blocks. Do not use indented code blocks in any new tutorials! Fenced code blocks allow you to specify the language of a code sample and are easier to edit.

```
// Code within fenced code blocks should be left-aligned!
print("Hello, Make School!")
print("Follow each language's style guide.")

if containsIndentation {
  print("Be consistent with number of spaces in indentation.")
}
```

### Overriding auto-detected language

Linguist will sometimes fail to classify a code sample's language correctly. When this happens (you'll notice while checking `ms-markdown-preview`), label the code block with the correct language.

#### This is incorrectly classified as Ruby

```
<h1>Hello, Rails!</h1>
```

#### This forces Highlight to recognize it as HTML

```html
<h1>Hello, Rails!</h1>
```

This works for most languages we use at Make School (html, css, js, pug, etc.). Make sure to preview them in `ms-markdown-preview` to insure that they appear correctly.

# Action highlights

Read about the following boxes and use them when appropriate.

## Quote box

Use quote boxes to include a quote.

> I think everyone should learn how to program a computer, because it teaches you how to think. I view computer science as a liberal art, something everyone should learn to do.
>
> - Steve Jobs

## Info box

Use info boxes to draw a students attention to an important concept.

> [info]
> Important concepts should be recapped or summarized in info boxes.

## Action box

Use action boxes whenever the student should do something (add code, implement pseudocode, change IDE settings, download files, etc).

> [action]
> Add the following import statement to the top of _TimelineViewController.swift_:
>
```
import ConvenienceKit
```
>
> This is still part of the box! Remember, code blocks need an empty line above them. In the case of code blocks inside of boxes, the line before and after a code block should only contain a `>` character.

This is no longer part of the box.

## Solution box

Use solution boxes to keep a solution hidden until the student hovers over it. These should be placed after a student has been asked to try implementing something themselves.

> [solution]
> This content is hidden until the user hovers over the box. Check it out with ms-markdown-preview!
>
```
import ConvenienceKit
```

This is not part of the box.

## Stretch Challenge box

Use challenge boxes should be used for additional features the user might want to implement. Make sure to give it a header of **Stretch Challenge**, as plain "challenges" have a different meaning at Make School.

- "Challenge" means its still required for students to complete.
- "Stretch Challenge" means its optional for students to complete (for those who want an extra challenge)

An example below, but you don't need to use the three tick symbols:

```
# Stretch Challenge

> [challenge]
> Would you kindly add a high score popup?
>
> The game could use some social integration as well!

This is not part of the box.
```

## Boxes followed by boxes

### This will not render correctly

```
> [action]
> Try viewing this with ms-markdown-preview!

> [info]
> The renderer will treat these as the same box :(
```

### This will render correctly

> [action]
> Try viewing this with ms-markdown-preview!

<!--  -->

> [info]
> Adding an empty comment forces the renderer to treat these as separate boxes :D
>
> The comment needs an empty line above and below it!

## Code blocks within action highlight boxes

> [info]
> Fenced code blocks exit prematurely if they contain an empty line while within an action highlight box. **To fix this, you will need to include a `>` on each empty line within the fenced code block!**
>
```
import ConvenienceKit
>
func doesNothing() {
>
}
```
>
> This will not render correctly without the `>` on empty lines within the fenced code block.

## Ordered/Unordered lists within action highlight boxes

You need to provide a new line with `>` before starting a list. See the examples below:

>[action]
> Below is a list:
>
> - item 1
> - item 2
> - item 3

<!-- -->

>[info]
> Below is a list:
>
> 1. item 1
> 1. item 2
> 1. item 3

## Syntax Formatting Within Code Blocks

We have two new tags that can be added into code blocks to give you some control over formatting.

`[none]` will keep things from being passed through syntax highlighting. This can be useful when showing terminal output.
`[bold]` will bolden the text after syntax highlighting is applied. This can be useful for bringing attention to newly added lines of code.
Make sure to always include the closing tag.
Tags can span multiple lines, but should not be added midline or interrupt code statements.
Tags cannot be combined currently. DM Dion on Slack if you need this functionality and we can explore how this can be added.

Example:

```
// Code within fenced code blocks should be left-aligned!
print("Hello, Make School!")
[none]print("This has no syntax highlighting")[/none]

[bold]if bold {
  print("It displays bold like this")
}[/bold]
```
