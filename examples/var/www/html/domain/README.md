# Complete Guide: Setting Up a Vue.js Project

This guide will walk you through the process of creating a new Vue.js project and starting the development server.

## Prerequisites

- [Node.js](https://nodejs.org/) (version 14 or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- [Vue CLI](https://cli.vuejs.org/) (optional, for Vue 2 projects)

## 1. Install Vue CLI (Optional for Vue 2)

If you want to use Vue CLI (for Vue 2 projects):

```bash
npm install -g @vue/cli
```

## 2. Create a New Vue.js Project

### Using Vue CLI (Vue 2 or Vue 3)

```bash
vue create my-vue-app
cd my-vue-app
```

Follow the prompts to select your preferred configuration.

### Using Vite (Recommended for Vue 3)

```bash
npm create vite@latest my-vue-app -- --template vue
cd my-vue-app
```

## 3. Install Dependencies

Inside your project directory, run:

```bash
npm install
```

## 4. Start the Development Server

To launch the development server, run:

```bash
npm run dev
```

- The server will start, and you will see a local URL (e.g., `http://localhost:5173/`).
- Open this URL in your browser to view your Vue.js application.

Please refer to our NGINX configuration for SSL purposes.

## 5. Next Steps

- Edit source files in the `src/` directory to start building your app.
- The development server supports hot module replacement for a smooth development experience.

## Troubleshooting

- If you encounter errors, ensure Node.js and npm are correctly installed.
- Check the official [Vue.js documentation](https://vuejs.org/) for more details.

---

You are now ready to develop with Vue.js!