# Beda Software - Frontent project generator

This generator helps to create predefined frontend (web and mobile) applications compatible to an [Aidbox](https://docs.aidbox.app/) app.

### What’s Included?
- A web application based on the create react app typescript template 
- A React Native mpbile application
- A shared repository with default FHIR and Aidbox resources type declarations
- Shared ESLint, Prettier and Git configuration files
- CI/CD files (Docker, GitLab) including files to run tests using Aidbox

(?) Two index.d.ts files?

### What’s the structure of a new created project?
```
frontend
└───chart
└───mobile (you can choose the name of this folder)
└───node_modules
└───shared
└───web
└───chart
│   other files
```

## Usage (if you want to create a new frontend project)

1. Install a [Yeoman](https://www.npmjs.com/package/yo) globally:

```
npm install -g yo
```

2. Run this generator:

```
npx yo beda
```

3. Reply to questions:

* ```What do you want to create:``` Choose "Project".

* ```Path to monorepo git repository:``` Hit "Enter" to use default template. If you want to use another template, provide a path to the git repository with another template. Can I provide a link to a local directory?

* ```Your mobile project name:``` Provide a name for mobile app directory that will be added to the frontent directory, e.g. "mobile". Wait while generator is installing project files in the "frontend" directory.

4. Go to the "frontend" directory:
```
cd ./frontend
```

5. Run the project:
```
yarn start
```
- > (?) How can I start ony web or mobile app?

7. Then open http://localhost:3000/ to see your web app.

- > (?) How can see a mobile app?


# Development (if you want to change this generator or its templates)

This template includes:

- Template for monorepo (shared files, common settings including linters, ci/cd and etc)
- Template for mobile (ios/android)
- Template for web

For development - clone the repo then try to run application generator:

```
git clone git@github.com:beda-software/frontend-beda-software-stack.git
cd ./frontend-beda-software-stack
npx yo ./generator-beda/generators/app
```

Set the current repo path as `.` as answer for the following question:

```
? Path to monorepo git repository (https://github.com/beda-software/frontend-beda-software-stack.git)
```
