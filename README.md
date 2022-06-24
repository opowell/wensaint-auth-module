<h1 align="center" >🔑 Auth Module</h1>
<p align="center">Zero-boilerplate authentication support for Nuxt.js!</p>

<p align="center">
<a href="https://auth.nuxtjs.org">具体使用请参照官方文档</a>
</p>

## 修改说明
本项目在原项目基础上实现了cookie与localStorage节点的runtime配置，使用示例如下
```
publicRuntimeConfig: {
	auth: {
	  cookie: {
		prefix: 'test.',
		options: {
		  path: '/',
		  maxAge: 2 * 3600
		}
	  },
	  localStorage: {
		prefix: 'test.'
	  }
	}
}
```

## Development

Running demo for development:

```bash
$ yarn install
$ yarn dev
```

Running tests for development:

```bash
$ yarn build
$ yarn nuxt build test/fixture
$ yarn jest
```

## License

[MIT License](./LICENSE) - Copyright (c) Nuxt Community
