# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:

- Examples of semantic and non-semantic tags
- The differences between semantic and non-semantic tags
- The benefits of using semantic tags (when possible)

### Response 1

**Semantic** HTML tags are tags that clearly and literally describe the information that they hold based off of their name. Semantic means **related to meaning in language**, which is how you can remember that they will display the element that they are named after.

**For example :** `<footer> <table> <nav>` are semantic tags, they contain and display exactly what their tags mean... a footer, a table, and a nav bar.

**Non-Semantic** HTML tags do not have explicit meanings in their names. It is unclear what is inside of this element just by the name.These tags act as containers for other HTML elements.

**For example :** `<div> <span>` are non-semantic tags.

The benefit of using semantic tags is _clarity_. The goal is to always make your code as clear and legible as possible. Semantic tags **quickly communicate the purpose** and content of HTML elements, making it easy for others to scan, read, and understand.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

Web accessibility is a crucial aspect of design that every developer must consider. Good design considers how people of all kinds will **use/interact** with their product. Making our websites accessible not only makes them available to those that are blind or visually impaired, but also to those that are not technically literate. Having an intuitive legible website grants access to those who are not savvy with web navigation.

Some examples of making web design more accessible are **captions, easy to digest colors, and clear alt texts for images.**

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;">hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

**Inline CSS Styling:** Useful for when you are making an extremely specific change to an HTML element.

**Separate CSS Styling:** Useful for when you want to batch style HTML elements of a specific _class_ or _id_. Many times we will be making **batch changes** to elements that belong to a specific group, for example, if we wanted to change all `h1` elements to purple, this would take 2 lines of code in a separate CSS file. If we were to use inline styling, we would have to manually change every single `h1` element.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

- An explanation of the concept of "classes" and "ids" with an analogy.
- An example of the usage using an HTML code block and a CSS code block.
- An explanation of the syntax using the terms: **attribute**, **selector**

### Response 4

In HTML, we have the option to label elements with grouping/labels called **attributes.** The `class` attribute is a type of grouping given to elements that share something in common. Many different elements can belong to the same class; they're designed to group similar elements with ease. The `id` attribute is used on a singular HTML element as a unique identifier. HTML elements can have multiple `class` attributes but only one `id` attribute.

For example, if we view every student at Marcy as an **HTML element**, our elements would all have the `class` _attribute_ of `class="marcy-lab-student"`. If class is rescheduled, a change would be made for all students. To update every student's schedule, we can reference this class instead of changing each Marcy student's schedule individually.

In this same example, we would use an `id` _attribute_ on each student individually. My HTML element would include something like this `id="autumn-lydon"` in addition to the class attribute mentioned above. If a coaching session needed to be scheduled, in CSS we would address my specific `id` attribute instead of the `class` attribute.

To reference attributes in CSS, we use _selectors_. A `class` selector will use a `.` in front of the class name. An `id` selector will use a `#` before the id name.

```html
<h1 class="marcy-lab-student" id="autumn-lydon">Autumn Lydon</h1>
```

```css
.marcy-lab-student {
  //updates the schedule of every element of this class (in theory)

  technical-lecture: "4PM";
}

#autumn-lydon {
  //updates only my element

  coaching-convo: "2PM";
}
```

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

The **DOM API** has specific functions built-in that allow it to interact with, select, and edit HTML elements. These functions are performed and belong in our **JS file.**

It is best practice to keep each file type as separate as possible for clarity and organization. When we combine all of these different elements and data types in a single file, it becomes very muddled and confusing not just for us, but for others too. If I were to look at your codebase, it should be very clear where the HTML, CSS, and JS lives. (In their own respective files)

When it comes to page layout and styling we should always leave that to our **HTML and CSS files**. When it comes to dynamic, changing elements, or adding functionality, we should use our **JS file** for that.
