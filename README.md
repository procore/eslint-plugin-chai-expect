To NPM Install This Do The Following:
http://blog.ilovacha.com/2014/01/17/fork-and-patch-npm-moduels-hosted-on-github/

Go to fork's page

Go to commits

On the right side of the commit you want to use click "Browse code"

On the browse code page right-click on "Download ZIP" button (or whatever it is that you are seeing) and copy the URL. It should be something like this https://github.com/SoftwareMarbles/express-jsend/archive/fdd4089087d916fa6e3b5abaa1ff9dd9ea96df8d.zip.

Edit that URL replacing archive with tarball and removing the .zip extension. You should end up with something like https://github.com/SoftwareMarbles/express-jsend/tarball/fdd4089087d916fa6e3b5abaa1ff9dd9ea96df8d.

Paste that into your package.json instead of the version. Like this:
"express-jsend": "https://github.com/SoftwareMarbles/express-jsend/tarball/fdd4089087d916fa6e3b5abaa1ff9dd9ea96df8d"  

And that's it - npm install works as it should and installs the module from the link.

# eslint-plugin-chai-expect

[![Build Status](https://img.shields.io/travis/Turbo87/eslint-plugin-chai-expect/master.svg)](https://travis-ci.org/Turbo87/eslint-plugin-chai-expect)

ESLint plugin that checks for common chai.js expect() mistakes


## Installation

```
npm install eslint-plugin-chai-expect
```


## Configuration

Add a `plugins` section and specify `chai-expect` as a plugin:

```json
{
  "plugins": [
    "chai-expect"
  ]
}
```

Enable the rules that you would like to use:

```json
{
  "rules": {
    "chai-expect/missing-assertion": 2,
    "chai-expect/terminating-properties": 1
  }
}
```


## Rules

- `no-inner-compare` - Prevent using comparisons in the `expect()` argument
- `missing-assertion` - Prevent calling `expect(...)` without an assertion like `.to.be.ok`
- `terminating-properties` - Prevent calling `to.be.ok` and other assertion properties as functions


## License

eslint-plugin-chai-expect is licensed under the [MIT License](http://www.opensource.org/licenses/mit-license.php).
