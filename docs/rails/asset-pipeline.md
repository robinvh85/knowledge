# Asset pipeline

- Asset pipeline is used to handle client-side code in Rails applications

## The old way to handle client-side code
- We typically had to put all of our assets in the public folder. Usually we ended up with a lot of files and it became difficult to know if they are being used or not.

## Convension for pipeline on Rails
- Our assets live in the `app/assets` folder, and there are also `lib/assets` and `vendor/assets` folders
- Assets are compiled on-the-fly in development and need to be precompiled in production
- We also have asset fingerprinting so the digest of the asset content becomes part of the filename itself to provide automatic cache busting.

## Sprockets gem
- Sprockets makes it possible to compile and serve all assets. Sprockets defines a processor pipeline so you can extend the way your assets are processed.
- [How sprockets works](https://github.com/rails/sprockets/blob/main/guides/how_sprockets_works.md)

## Importmap
- File config: `config/importmap.rb`
- Import maps let you import JavaScript modules using logical names that map to versioned/digested files – directly from the browser.
- So you can build modern JavaScript applications using JavaScript libraries made for ES modules (ESM) without the need for transpiling or bundling. 
- This frees you from needing Webpack, Yarn, npm, or any other part of the JavaScript toolchain.

## Reference
