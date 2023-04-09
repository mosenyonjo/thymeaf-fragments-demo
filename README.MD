# Thymeleaf Fragments Demo

A demo project using Thymeleaf fragments and version-agnostic webjars approach.

## HTML Structure

- `<head>` section: Defines a header for a document or section. Contains metadata about the document, including the title of the page, links to external stylesheets, scripts, and other information.

- `<body>` section: Contains the visible content of the page, including headings, paragraphs, images, videos, links, forms, and other elements.

- `<header>`: Defines a header for a document or section. Typically located at the top of the page, contains branding, logos, navigation menus, and other elements related to the site's overall design.

- `<main>`: Defines the main content of a document. The primary content of the page, including articles, blog posts, product listings, and other information.

- `<article>`: Defines an independent, self-contained piece of content.

- `<nav>`: Defines a set of navigation links.

- `<section>`: Defines a section of a document.

- Sidebar/aside: Defines content aside from the content (like a sidebar). An optional section located alongside the main content, which can contain additional information, links, or advertising.

- `<footer>`: Defines a footer for a document or section. Typically located at the bottom of the page, contains copyright information, contact information, and links to social media and other resources.

---
## Thymeleaf Fragment Syntaxes

There are different syntaxes that can be used to include fragments in Thymeleaf templates:

1. Fragment inclusion using `th:replace`: This syntax replaces the content of the tag with the fragment. The `th:replace` attribute is used to specify the fragment to be included.

   <div th:replace="fragments/header :: header"></div>

2. Fragment inclusion using `th:include`: This syntax includes the fragment inside the tag. The `th:include` attribute is used to specify the fragment to be included.

   <div th:include="fragments/footer :: footer"></div>

3. Fragment inclusion using `th:fragment`: This syntax defines a fragment in the template that can be included in other templates. The `th:fragment` attribute is used to define the fragment.

   <!-- Define a fragment in the template -->
   <div th:fragment="header">
       `<h1>'Header Content`</h1>`
   </div>

   <!-- Include the fragment in another template -->
   <div th:replace="fragments/header :: header"></div>

4. Fragment inclusion using `th:insert`: This syntax inserts the fragment at the location specified by the `th:insert` attribute.

   <div th:insert="fragments/sidebar :: sidebar"></div>

Note that the syntax used for fragment inclusion may vary depending on the specific requirements of your application.

Sources:
- [Maven WebJars](https://www.baeldung.com/maven-webjars)
