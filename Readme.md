# Deno development in Emacs

## Prerequisites

- Make sure you have [tide](https://github.com/ananthakumaran/tide) installed and setup


## Setup to enable Deno support for your own project

- `npm init -y` to setup a `package.json` (we need this as we install dependencies using `npm`)
- `npm install --save-dev typescript-deno-plugin typescript` as [described in typescript-deno-plugin repo](https://github.com/justjavac/typescript-deno-plugin#with-vs-code)
- finally, add the following to your `tsconfig.json` to enable the `typescript-deno-plugin`
  ```json
  {
    "compilerOptions": {
      "plugins": [{
          "name": "typescript-deno-plugin",
          "enable": true, // default is `true`
          "importmap": "import_map.json"
      }]
    }
  }
  ```

With this in place, `tide` will function just as expected with a codebase targeted to `Deno` as it does with a normal `TypeScript` project.

![Working deno and emacs integration screenshot](https://user-images.githubusercontent.com/635512/83182847-41535c00-a127-11ea-83ca-ffb4dcdccf23.png)
