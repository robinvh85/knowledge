# Module System
- Trước khi chuẩn ES2015 (ES6) ra đời, Javascript không hỗ trợ cho các lập trình viên bất kỳ một phương thức tự nhiên nào để tổ chức hệ thống code. Node.js được tạo nên từ Javascript, tuy nhiên những người viết ra Node.js đã đưa thêm vào `CommonJs` để giải quyết vấn đề về "cấu trúc" hệ thống code viết bởi Javascript.

## Module
- A module is just a piece of code in a file that you can call and use from other files. A modular design is the opposite of having all your project's code in one single file.

## Types of modules
- As JavaScript was first created to be just a small scripting language for websites, a feature for big projects like modules wasn't supported at the beginning.
- But as the language and the ecosystem grew, developers started to see the need for this feature. And so different options and libraries were developed to add this feature to JavaScript.
- Of the many available, we're only going to take a look at CommonJS and ESmodules, which are the most recent and widely used ones.

## CommonJS modules
- CommonJS is a set of standards used to implement modules on JavaScript. The project was started by Mozilla engineer Kevin Dangoor in 2009.
- CommonJS is mainly used in server-side JS apps with Node, as `browsers don't support the use of CommonJS`.
- As a side comment, Node used to only support CommonJS to implement modules, but nowadays it also supports ESmodules which is a more modern approach.

## ESmodules
- ESmodules is a standard that was introduced with ES6 (2015). The idea was to standarize how `JS modules work and implement this features in browsers` (which didn't previously support modules).
- ESmodules is a more modern approach that is currently supported by browser and server-side apps with Node.

## Import-maps
- This proposal allows control over what URLs get fetched by JavaScript import statements and import() expressions. This allows "bare import specifiers", such as import moment from "moment", to work.
- To use import-maps for all browser, it should be use [ES Module Shims](https://github.com/guybedford/es-module-shims#usage) by add code below:
```html
<script async src="https://ga.jspm.io/npm:es-module-shims@1.5.18/dist/es-module-shims.js"></script>
```

## Reference
- [Modules in Javascript](https://www.freecodecamp.org/news/modules-in-javascript/)
- [Tìm hiểu về module system](https://viblo.asia/p/tim-hieu-ve-module-system-commonjs-va-require-QpmleL3mZrd)
- [Import maps](https://github.com/WICG/import-maps#the-basic-idea)