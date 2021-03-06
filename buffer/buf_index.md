<!-- YAML
type: property
name: [index]
-->

* `index` {integer}

索引操作符 `[index]` 可用于获取或设置 `buf` 中指定的 `index` 位置的八位字节。
该值指向单个字节，所以有效的值的范围是 `0x00` 至 `0xFF`（十六进制）、或 `0` 至 `255`（十进制）。

该操作符继承自 `Uint8Array`，所以对越界访问的行为与 `UInt8Array` 相同。
也就是说，取值时返回 `undefined`，赋值时不作为。

```js
// 拷贝 ASCII 字符串到 `Buffer`，每次拷贝一个字节。

const str = 'http://nodejs.cn/';
const buf = Buffer.allocUnsafe(str.length);

for (let i = 0; i < str.length; i++) {
  buf[i] = str.charCodeAt(i);
}

console.log(buf.toString('ascii'));
// 打印: http://nodejs.cn/
```

