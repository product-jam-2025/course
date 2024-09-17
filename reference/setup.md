# Software setup for the course

In order to have all the required software for this course, you must follow this setup guide completely.

## Apps

### VS Code

We are using VS Code for our code editor. You may have other personal preferences, but please use VS Code for this course. It has superior support for JavaScript and React development, and our starter kit for web development in this course is configured to leverage VS Code functionality.

- **[Install VS Code from this location](https://code.visualstudio.com)**

VS Code has an extensive ecosystem of extensions. Please install the following extensions (we may not use them all):

- **[ES Lint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)**
- **[HTML CSS](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)**
- **[Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)**
- **[GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)**
- **[GitHub Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)**

### Chrome or Chromium

Different web browsers hav varying levels of support for web standards. We will be using Google Chrome for this course, but you can use Chromium if you prefer.

- **[Install Google Chrome from this location](https://www.google.com/chrome/)**
- **[Install Chromium from this location](https://www.chromium.org/developers/how-tos/get-the-code/)**

Chrome/Chromium has an extensive ecosystem of extensions. Please install the following extensions (we may not use them all):

- **[React Dev Tools](https://chromewebstore.google.com/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)**
- **[JSON Formatter](https://chromewebstore.google.com/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa)**

## Websites

You need active accounts on the following websites. **Create your GitHub account first**, and use it to log in to the other services.

- **[Github](https://github.com)** - We use this to host our code and submit development assignments.
- **[Vercel](https://vercel.com)** - We use this to deploy our code as a web application, accessible on the public Internet.
- **[Supabase](https://supabase.com)** - We use this as a database services for our web application.

Additionally, please bookmark the following websites:

- **[Phind](https://www.phind.com)** - An interface for pair programming with AI.
- **[MDN](https://developer.mozilla.org/en-US/)** - A large library of high quality resources for web development.
- **[React](https://react.dev)** - Documentation for react, a user interface library we will be using.
- **[Next.js](https://nextjs.org)** - Documentation for Next.js, a framework for building web applications with React.

## Development software

We are writing all our code in JavaScript (or a superset of JavaScript called TypeScript). All browsers have a built in JavaScript runtime. Additionally, some of our code needs to run on a server, and for that we need a JavaScript runtime for our local development - Node (we will talk in the course about client-server architecture in the context of web development).

- **[Node LTS v18](https://nodejs.org/en/download)** - Node is a JavaScript runtime. We will use it to run our server-side code.
- **[Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)** - Git is for version control. We will use it to manage our code.

## Verification

Once you have installed all the required software, please verify that everything is working correctly. Below is a minimal set of steps to perform in order to do that.

1. Email your GitHub username to teaching staff. Once you do this, they will add you to the GitHub organization for this course, and you will then be able to perform the rest of the steps.
2. Create your own copy of the [starter codebase](https://github.com/digital-product-jam-2024/starter-kit):
   - Make sure your copy lives under your own username, not that of the course. i.e.: https://github.com/<YOUR_USERNAME>/<YOUR_COPY_NAME>
   - Do this by following the steps described over here: [GitHub Docs](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
   - Give your repository a name that is unique to you, for example `starter-username`
3. Clone the remote repository to your local computer using Git from your development machine:
   - **[git clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)**
4. Visit the repository directory on your local filesystem, and open it in VS Code
   - [via the command line](https://code.visualstudio.com/docs/editor/command-line#_launching-from-command-line)
   - or [via the app](https://code.visualstudio.com/docs/introvideos/basics)
5. You should now have VS Code open at the folder of the Git repository that you cloned from your GitHub account. Click on the `README.md` file to open it in VS Code.
6. Follow the instructions in the `README.md` file to:
   - Install project dependencies
   - Run the server
   - See the running app in a browser
