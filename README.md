# Hash Viewer

You can use this to store entire documents in URLs. It is similar to [Hashify](https://hashify.me) but has a simpler presentation, uses LZ-based compression via [lz-string](https://github.com/pieroxy/lz-string), and supports LaTeX math input via [MathJaX](https://www.mathjax.org/). It is hosted on [GitHub Pages](https://pages.github.com/) and uses [marked](https://marked.js.org/) for markdown processing.

The page is styled using a modified version of [LaTeX.css](https://latex.now.sh/).

This service is especially useful for sharing text content with simple formatting and math. It can also be useful for storing human readable information on NFC tags. The information opens in a browser, yet will be entirely contained on the tag.

This project is fully client side, so no data is stored on the server. While I cannot read anything written or viewed using this site, the full hashes may be contained in your browser history. Because these hashes technically contain the full content of the page, you should keep this in mind if sharing sensitive data.

The main page where hashes are decoded is `404.html`. This exploits the fact that all unknown urls on GitHub Pages are directed to the 404 page. By using 404, we ensure that every hash url is sent to this page.

The code is very short and simple. Decoding of hashes is handled by [404.js](/assets/js/404.js) and encoding is handled by [index.js](/assets/js/index.js).