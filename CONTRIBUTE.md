# For Contribution

- Clone the repository and run it locally.
- Do changes according to the requirements.
- Use this command for creating ```/dist``` folder:
```npx tailwindcss -i ./src/index.css -o ./dist/index.css --watch```

 - Update the ```exports``` in ```package.json```.

 - Test the changes locally and be sure about the changes.
 - Always create a Good Pull Request for your changes to get merged.
 - Do not raise PR for small changes like spelling correction, etc. The contribution must be meaningful.
- Always try to add description of the PR to give an elaborative explanation of the PR and a meaningful PR name.

 ## Common Commands:

- Run Locally - ```npm run dev```
- Build - ```npm run build```
- Test - ```npm run test```
- eject - ```npm run eject```

### For testing the package locally:

1. Run ```npm link``` to make the package available locally.
2. Create a new project and run ```npm link <package-name>```.

Now its imported in ```node_modules``` of the new project. You can use it as a package.