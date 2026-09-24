Event Delegation Demo — JavaScript & Tailwind CSS

Interactive front-end demo created to demonstrate Event Delegation with Vanilla JavaScript, the DOM API, dynamic DOM elements and a responsive interface built with Tailwind CSS.

🎯 Objective

The goal of this project is to show, through a practical interface, how a single event listener attached to a parent element can manage interactions with multiple child elements.

The demo also shows that elements added dynamically can use the same listener without registering a new eventListener for each button.

✨ Features

Event Delegation with a single click listener

Dynamic DOM element creation

Dynamic project selection

Project preview updated according to the selected item

New projects can be added at runtime

Same event listener works with dynamically added projects

Responsive layout for desktop, tablet and mobile

Tailwind CSS utility classes

Interactive hover and selected states

Smooth UI transitions

Accessible semantic/ARIA attributes

SEO metadata and structured data

🧠 Event Delegation

Instead of attaching an event listener to every project button, the demo listens for clicks on the parent project list:

list.addEventListener("click", (e) => {
  const button = e.target.closest(".item__button");

  if (!button) return;

  const item = button.closest(".item");
  const projectId = item.dataset.project;

  showProject(projectId);
});

When a new project is added dynamically, no new listener is required.

This is the main concept demonstrated by the project.

🔧 Concepts demonstrated

Event Delegation

Event Bubbling

Event Listener

DOM API

closest()

dataset / data-* attributes

Dynamic DOM manipulation

Dynamic elements

Responsive Design

Tailwind CSS

Front-End Development

🛠️ Technologies

HTML5

Vanilla JavaScript

Tailwind CSS

DOM API

CSS / responsive utilities

Tailwind CSS is loaded through the CDN, so no build process is required for this demo.

📱 Responsive Design

The interface adapts to different screen sizes:

Mobile: content is displayed in a single column and project buttons become full-width.

Tablet: the interface remains stacked to preserve readability and spacing.

Desktop: the hero and project/preview sections use a multi-column layout.

The responsive behavior is implemented with Tailwind CSS responsive utilities.

🚀 Run the project

No installation is required.

Clone the repository:

git clone https://github.com/YOUR-USERNAME/event-delegation-demo.git

Open index.html in your browser.

Because Tailwind CSS is loaded from the CDN, an internet connection is required when opening the page.

📂 Project structure

event-delegation-demo/
├── index.html
└── README.md

🔍 SEO

The HTML page includes:

SEO title

Meta description

Keywords

Author metadata

Robots directive

Open Graph metadata

Twitter/X metadata

JSON-LD structured data

Semantic HTML and ARIA attributes

👩‍💻 Author

Asma Hammami

Front-End Developer / Web Integrator

Topics

JavaScript Event Delegation DOM Tailwind CSS Responsive Design Front-End Development Web Development Dynamic DOM

⭐ A small practical demo focused on clean event handling and responsive front-end integration.
