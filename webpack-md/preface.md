# 前言

介绍前端模块系统的演进历史，以及 Webpack 出现的背景及其特点。

而webpack就不同了，webpack的哲学是一切皆是模块，无论是js/css/sass/img/coffeejs/ttf….等等，webpack可以使用自定义的loader去把一切资源当做模块加载，这样就解决了模块依赖的问题，同时，利用插件还可以对项目进行优化，由于模块的加载和项目的构建优化都是通过webpack一个”人“来解决的，所以模块的加载和项目的构建优化并不是无机分离的，而是有机的结合在一起的，是一个组合的过程，这使得webpack在这方面能够完成的更出色，这也是webpack的优势所在。

- 1、过去使用require和rjs等进行模块加载的方式，可以替换为webpack提供的指定loader去完成，你也可以自己开发加载特定资源的loader。
- 2、过去使用gulp和grunt完成项目构建优化的方式，可以替换成webpack提供的插件和特定的配置去完成。
- 3、由于模块的加载和项目的构建优化有机的结合，所以webpack能够更好的完成这项工作
- 4、并不是说有了webpack就淘汰的gulp等，有些特定的任务，还是要使用gulp去自定义完成的。但是不保证webpack的未来发展趋势会怎么样。

最后，给大家分享一个官方的教程，教程链接：http://blog.madewithlove.be/post/webpack-your-bags/