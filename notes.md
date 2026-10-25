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
