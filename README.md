# rollup

1.安装
```
npm install --save-dev rollup
```

2.根目录下新建rollup.config.js
```
export default {
  input: './src/main.js',
  output: {
    file: './dist/js/main.min.js',
    format: 'iife'
  }
}
```
> 配置的含义：
>> input： rollup先执行的入口文件。<br>
>> output：rollup 输出的文件。<br>
>> output.format: rollup支持的多种输出格式(有amd,cjs, es, iife 和 umd, 具体看 http://www.cnblogs.com/tugenhua0707/p/8150915.html)<br>
>> sourceMap —— 如果有 sourcemap 的话，那么在调试代码时会提供很大的帮助，这个选项会在生成文件中添加 sourcemap，来让事情变得更加简单。

3.package.json添加
```
"scripts": {
  "build": "rollup -c"
}
```

4.npm run build