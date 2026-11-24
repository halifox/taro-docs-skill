# Stats

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/files/Stats)

描述文件状态的对象

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| lastAccessedTime | `number` | 文件最近一次被存取或被执行的时间，UNIX 时间戳，对应 POSIX stat.st\_atime |
| lastModifiedTime | `number` | 文件最后一次被修改的时间，UNIX 时间戳，对应 POSIX stat.st\_mtime |
| mode | `string` | 文件的类型和存取的权限，对应 POSIX stat.st\_mode |
| size | `number` | 文件大小，单位：B，对应 POSIX stat.st\_size |

<a id="isdirectory"></a>

### isDirectory

判断当前文件是否一个目录

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/Stats.isDirectory.html)

```tsx
() => boolean
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Stats.isDirectory | ✔️ |  |  |

<a id="isfile"></a>

### isFile

判断当前文件是否一个普通文件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/Stats.isFile.html)

```tsx
() => boolean
```

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Stats.isFile | ✔️ |  |  |

<a id="api-支持度-2"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Stats.isDirectory | ✔️ |  |  |
| Stats.isFile | ✔️ |  |  |
