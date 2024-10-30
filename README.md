# ANTEI take-home

## Project Overview
A take-home from (ANTEI)[https://anteihk.com]

## Project Structure
```
CompanyDashboard/
├─ src/                         # Source code/Components
│   └── components/             # Repository with components
        └──Banner.vue           # Welcome banner 
        └──ContactSection.vue   # Component with v0 prompt
        └──Footer.vue           # Info about copyright
        └──Navbar.vue           # header with navigation
        └──Partners.vue         # Partners of ANTEI
        └──WhyAI.vue            # 'How can AI help your buisness'
        └──WhyUs.vue            # About ANTEI's team  
├── main.js                  # Main JavaScript script
├── index.html               # Main html file to enter script
├── package.json             # Setting to run the project
├── .gitignore               # Git ignore file
├── README.md                # Project documentation
```
```
V0 promt for component 'Contact Us':

Create a Vue.js component that displays a "Contact" section. The section should be divided into two parts:
Left Side: "Contact Us" headinп, Company address, phone, and email information
Right Side: Form with fields for "Company name", "Full name", "Email", and "Message" "Message" field should be a vertically expandable textarea
Color Scheme: Black, white, purple, yellow
Please generate the code for this "Contact" section using Vue.js.

Result: v0 created a Vue.js component for a "Contact" section with the specifications I've provided. Used technologies: Vue 3 with the Composition API, some basic styling with Tailwind CSS.

```
## Branching Strategy
This project follows the Git Flow branching model:
- `master`: The production-ready branch.
- `dev`: The development branch where features are integrated.

## Getting Started

### Installation
1. Clone the repository:
    ```
    git clone https://github.com/minstired/homework.git
    cd homework
    ```

2. Initialization packet manager
    ```
    npm init
    ```
### Installing dependecies 

1. Installing TailwindCss
```
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init
    Настройка файла tailwind.config.js
    Настройка файла index.css
    Создание и настройка файла postcss.config.js
    Добавление импорта в main.js
```

2. Installing lucide-vue-next
```
    npm install lucide-vue-next
```
3. Installing sass
```
    npm install -g sass
```

### Running the Project
```
    npm run dev  # Start project on a local-server
```
