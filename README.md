In this tutorial I will explain the setup for tailwindcss 2.0.1. I found the documentation is hard to follow and Adam's YouTube [video](https://www.youtube.com/watch?v=21HuwjmuS7A) kind of outdated.

First, create a directory with your project name, here I created a project named `tailwind-helloworld`.
```bash
mkdir tailwind-helloworld 
```
Run the npm command - `npm init -y`  to create a package.json with defaults.

Install tailwindcss and deps with the command
`npm install tailwindcss postcss autoprefixer postcss-cli`

These are the installed versions, 
```
+ autoprefixer@10.0.4
+ postcss@8.1.10
+ postcss-cli@8.3.0
+ tailwindcss@2.0.1
```
`touch postcss.config.js`

Include the following content in `postcss.config.js` file,
```javascript
module.exports = {
    plugins: {
      tailwindcss: {},
      autoprefixer: {},
    }
}
```

```npx tailwindcss init``` will initialise tailwindcss configuration.
Include the build command in package.json, and execute `npm run build`. 
```json
"scripts": {
    "build": "postcss src/css/*.css -o dist/css/compiled.css"
  }
```
That's it!!!!

You are good to reference build css file in your html code.
