# Teams Core Documention
## How to use documentation

Through this applications code are symbolic linked "README.md" files that point back to MarkDown files in the `/docs` folder. This is that that documention is easy to find in context while browsing in a code reposiotry system like github.

The Actual documentation is all located in the `/docs` folder and is build as a static website on the branch `gh-pages`.

### Update Documentaion

Change or add a md file in the docs directory and add it to the `/.mkdocs.yml` "nav" section.

If you would like this file to also appear in a specific folder of the code you can sym link it like so.

=== "Powershell"
    ``` powershell
    New-Item -ItemType SymbolicLink -Path "./src/code/directory/README.md" -Target "./docs/myInfoName.md"
    ```

=== "Bash"
    ``` bash
    ln -s ./docs/myInfoName.md ./docs/myInfoName.md
    ```

### Run Documentation Site Locally

1. [Install mkdocs](https://www.mkdocs.org/user-guide/installation/)
2. [Install Material theme](https://squidfunk.github.io/mkdocs-material/getting-started/)

Serve Locally:
`mkdocs serve`

### Publish Documention to github
`mkdocs gh-deploy`

This command will create/update the documentation branch `gh-pages` with the static output. Once pushed to github the pages site will automaticly update.

### Why is the documention first? It's annoying
Akin to learning where the brakes on a car are, this is for project integrity. You will not be the only person writing code for this project. Please leave a lagacy of purposeful documention.


## Getting Started
This is a TypeScript based React App w/Material-Ui at it's core.

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).