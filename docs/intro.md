---
sidebar_position: 1
---

# Project Setup

Quickstart for **Infinite Gamings in less than 10 minutes**.

## Getting Started

Get started by **cloning our repositories**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.
- [Repositories](https://github.com/team-embers) required to have a github account & SSH key.
- [Package Managers](https://github.com/team-embers)
  - [Yarn](https://yarnpkg.com/) or [NPM](https://www.npmjs.com/)
- [ReactJS](https://reactjs.org/) need to have knowledge in ReactJS since, the frontend is built with react.
- [StrapiJS](https://strapi.io/) knowledgeable in MVC & javascript.
- [MongoDB](https://www.mongodb.com/) our database program.

## Run Backend

Backend is built with StrapiJS **Node.js Headless CMS**.

Important to not upgrade any packages especially strapi since strapi v4, support for mongodb is depreciated:

```bash
git clone https://github.com/team-embers/backend-infinite-gaming.git
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

```bash
yarn 
```

The command <strong><em>yarn</em></strong> installs all necessary dependencies you need to run our backend (you can also use npm install if youre using npm as your package manager).

## Start backend server

<strong>note:</strong> must create .env file and ask for env variables to devs assigned to the project.

Run the development server:

```bash
cd <directory-backend>
yarn develop
```

The `cd` command changes the directory you're working with. In order to work with your newly cloned backend project, you'll need to navigate the terminal there.

The `yarn develop` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:1338/.
