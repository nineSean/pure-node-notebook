
## 引入stream处理post和put请求 + 采用Promise构建流式中间件


------------------------------------------------------


http ==> on('data',()) response.end()
fs  fs.writeFile fs.readFile
console.log() ==> process.stdout

request.on('data',()=>{})
request.on('end',()=>)

1、stream知识 => 处理post请求 
2、抽象url-parser
3、Promise抽象中间件模型 + 链式处理static-server、api-server、url-parser中间件。


- [Promise复习](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise)

- [request对象](https://github.com/nodejs/node/blob/master/doc/api/http.md)

- [stream基本知识](https://github.com/nodejs/node/blob/master/doc/api/stream.md)



-----------------------node的url/querystring模块---------------

> 处理客户端url

[url模块](https://github.com/nodejs/node/blob/master/doc/api/url.md)

- [url模块图解](./3rd-assets/url.png)


> 处理客户端query参数

[querystring模块](https://github.com/nodejs/node/blob/master/doc/api/querystring.md)

```javascript
	querystring.stringify({ foo: 'bar', baz: ['qux', 'quux'], corge: '' })
	// returns 'foo=bar&baz=qux&baz=quux&corge='

	querystring.parse('foo=bar&abc=xyz&abc=123')
	// returns {
	  foo: 'bar',
	  abc: ['xyz', '123']
	}
```
