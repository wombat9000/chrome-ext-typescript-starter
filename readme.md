### Commands
`$ npm run build`: builds the project

`$ npm run test`: runs jest

`$ npm run lint`: runs the linter

### Testing the extension
1. Build the project with `$ npm run build`.
2. Visit `chrome://extensions` and activate developer mode. 
3. Click 'Load unpacked' and select the project directory.
4. Browse `https://amazon.com` and visit any product page.
5. Product name should be 'NewProductName'.


### How it gets into Chrome
- `$ npm run build` builds the application and puts the sources into `build/dist/` directory.
- `manifest.json` has references to the required files inside the `build/dist/` directory, aswell as config on
when and how to use the files.
- Upon loading the extension into chrome, `manifest.json` is inspected, and the required files are also loaded.