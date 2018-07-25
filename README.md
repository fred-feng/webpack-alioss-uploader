webpack4.0 plugin for aliyun oss upload

```
const AliossUploaderPlugin = require('webpack-alioss-uploader')
module.exports = {
	entry: './src/index.js',
	output: {
		path: path.resolve(__dirname, 'dist'),
		filename: 'bundle.js'
	},
	plugins: [
		new AliossUploaderPlugin({
			accessKeyId: '***',
			accessKeySecret: '***',
			region: 'oss-cn-hangzhou', // eg: oss-cn-hangzhou
			bucket: 'stgame',
			prefix: 's3/v1', // oss directory prefix; eg: auto_upload_ci/test
			exclude: /.*\.(html|js)$/,   // Optional, default: /.*/
			enableLog: true,        // Optional, default: true
		})
	]
}
```