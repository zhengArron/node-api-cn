<!-- YAML
added: v0.1.21
changes:
  - version: v7.6.0
    pr-url: https://github.com/nodejs/node/pull/10739
    description: The `path` parameter can be a WHATWG `URL` object using
                 `file:` protocol. Support is currently still *experimental*.
-->

* `path` {string|Buffer|URL}
* 返回: {boolean}

如果路径存在，则返回 `true`，否则返回 `false`。

有关详细信息，参阅此 API 的异步版本的文档：[`fs.exists()`]。

虽然 `fs.exists()` 已废弃，但 `fs.existsSync()` 不是废弃的。
`fs.exists()` 的 `callback` 参数接受与其他 Node.js 回调不一致的参数。
`fs.existsSync()` 不使用回调。

```js
if (fs.existsSync('/etc/passwd')) {
  console.log('文件已存在');
}
```

