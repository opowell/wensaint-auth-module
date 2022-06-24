<h1 align="center" >🔑 Auth Module</h1>
<p align="center">Zero-boilerplate authentication support for Nuxt.js!</p>

<p align="center">
<a href="https://auth.nuxtjs.org">Refer to the document before usage(具体使用请参照官方文档)</a>
</p>

## Modify Remark
The origin proect cant't support auth runtimeConfig. 
So i have to build again and again when I deploy the site within different subdomains(eg https://xxx.com/a and https://xxx.com/b), what a waste of time!!!

本项目在原项目基础上实现了cookie与localStorage节点的runtime配置，从而实现“一套代码、多处部署”，即使在同一个域名下也不会互相干扰。
使用示例如下
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
