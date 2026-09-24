# Event Delegation — JavaScript & Tailwind CSS

An interactive front-end demo showcasing **Event Delegation in JavaScript** with a responsive interface built using **Tailwind CSS**.

The project demonstrates how a single event listener attached to a parent element can handle interactions with multiple child elements — including elements that are added dynamically to the DOM.

## ✨ Demo

The interface contains a list of projects that can be selected to display their preview.

You can also add new projects dynamically using the **"Ajouter un projet"** button.

The important part of the demo is that newly added projects work with the same event listener without requiring a new listener for each button.

## 🧠 What is demonstrated?

### Event Delegation

Instead of attaching an event listener to every project button:

```javascript
button.addEventListener("click", ...)
```

the demo attaches a single listener to the parent container:

```javascript
list.addEventListener("click", (e) => {
  const button = e.target.closest(".item__button");

  if (!button) return;

  const item = button.closest(".item");
  const projectId = item.dataset.project;

  showProject(projectId);
});
```

This approach allows the same listener to handle both existing and dynamically created elements.

## 🎨 Features

* Event Delegation with JavaScript
* Dynamic DOM elements
* Interactive project selection
* Dynamic project creation
* Project preview updates
* Responsive interface
* Tailwind CSS styling
* Hover and selection states
* Smooth UI transitions
* No JavaScript framework required

## 🛠️ Technologies

* **HTML5**
* **JavaScript (Vanilla JS)**
* **Tailwind CSS**
* **DOM API**
* **Event Delegation**

## 📂 Project Structure

```text
event-delegation/
│
├── index.html
└── README.md
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/event-delegation.git
```

### 2. Open the project

Open `index.html` directly in your browser.

No build process or package installation is required.

## 💡 Why Event Delegation?

Event Delegation is particularly useful when working with lists, tables, menus, or interfaces where elements can be added or removed dynamically.

Instead of creating multiple event listeners, one listener on a parent element can handle events coming from its children.

This can make event handling simpler and easier to maintain.

## 👩‍💻 Author

**Asma Hammami**

Front-End Developer / Web Integrator

---

⭐ If you find this demo useful, feel free to explore the code and experiment with Event Delegation.
