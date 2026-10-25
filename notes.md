# HTTP Observations (Lab 4, Task 1)

| Question                                    | My Answer                     |
| ------------------------------------------- | ----------------------------- |
| Request method for index.html               | GET                           |
| Status code with Disable cache ticked       | 200 OK  |
| Status code on a normal reload              | |200 OK 
| Status code for /nothing-here.html          | 200 OK |
| Value of the Content-Type response header   | text/html; charset=UTF-8       |
| Remote Address (IP and port)                | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) |http://127.0.0.1:5500/index.html                         |

## Why is this address http and not https?

This address uses HTTP because the website is running on my own computer. The traffic stays on my computer, so HTTPS is not necessary for this local test.

## Specificity Experiment

When I used `#main p`, all paragraphs inside the main section became red because an ID selector has higher specificity than a class or element selector. When I changed it to `main p`, the hero paragraph kept its white colour because the `.hero p` selector was more specific.

## Selectors I Used

| Selector Type    | Example           | Purpose                                            |
| ---------------- | ----------------- | -------------------------------------------------- |
| Element          | `body`            | Styles all body elements.                          |
| Class            | `.site-header`    | Styles elements with this class.                   |
| ID               | `#main`           | Styles the element with this ID.                   |
| Grouping         | `h1, h2, h3`      | Applies the same styles to multiple elements.      |
| Descendant       | `.saved-orders p` | Selects paragraphs inside saved orders.            |
| Child            | `main > section`  | Selects sections directly inside main.             |
| Adjacent sibling | `h1 + p`          | Selects the paragraph immediately after a heading. |
| Compound         | `a.active`        | Selects links that also have the active class.     |
| Attribute        | `input[required]` | Selects required input fields.                     |
| Pseudo-class     | `a:hover`         | Styles a link when the mouse is over it.           |
| Pseudo-element   | `h2::before`      | Adds content before a heading.                     |

## Bug log (Lab 4, Task 6)

| # | What was wrong (file and line) | Which tool showed it | My fix |
|---|---|---|---|
| 1 | Missing page language in bugs.html | Validator / Accessibility | Added lang="en" |
| 2 | Navigation used a div in bugs.html | Accessibility Tree | Changed div to nav |
| 3 | Heading level skipped in bugs.html | Lighthouse / Accessibility | Changed h4 to h2 |
| 4 | Image had no alt text in bugs.html | Lighthouse | Added alt text |
| 5 | Label and input did not match in bugs.html | Lighthouse / Accessibility | Matched for and id |
| 6 | Wrong stylesheet path in bugs.html | Network | Linked bugs.css |
| 7 | Misspelled colour property in bugs.css | Styles Pane | Changed colour to color |
| 8 | Missing semicolon in bugs.css | Styles Pane | Added semicolon |
| 9 | CSS selector did not match in bugs.css | Styles Pane | Changed .notes to .note |
| 10 | Button had no explicit type in bugs.html | Code inspection | Added type="submit" |