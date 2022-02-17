---
sidebar_position: 1
---

# Run Backend

Backend is built with StrapiJS **Node.js Headless CMS**.

Important to not upgrade any packages especially strapi since strapi v4, support for mongodb is depreciated:

```bash
git clone https://github.com/team-embers/backend-infinite-gaming.git
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

```bash
yarn 
```

The command <strong><em>yarn</em></strong> installs all necessary dependencies you need to run our backend (you can also use <strong><em>npm install</em></strong> if youre using npm as your package manager).

## Start backend server

<strong>note:</strong> must create .env file and ask for env variables to devs assigned to the project.

Run the development server:

```bash
cd <directory-backend>
yarn develop
```

The `cd` command changes the directory you're working with. In order to work with your newly cloned backend project, you'll need to navigate the terminal there.

The `yarn develop` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:1338/.
