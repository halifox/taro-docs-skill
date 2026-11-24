# Taro.createWebAudioContext()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/audio/createWebAudioContext)

创建 WebAudio 上下文。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.createWebAudioContext.html)

<a id="类型"></a>

## 类型

```tsx
() => WebAudioContext
```

<a id="示例代码"></a>

## 示例代码

一个简单的播放demo

```tsx
const audioCtx = Taro.createWebAudioContext()

const loadAudio = (url) => {
  return new Promise((resolve) => {
    Taro.request({
      url,
      responseType: 'arraybuffer',
      success: res => {
        console.log('res.data', res.data)
        audioCtx.decodeAudioData(res.data, buffer => {
          resolve(buffer)
        }, err => {
          console.error('decodeAudioData fail', err)
          reject()
        })
      },
      fail: res => {
        console.error('request fail', res)
        reject()
      }
    })
  })
}

const play = () => {
  loadAudio('xxx-test.mp3').then(buffer => {
    const source = audioCtx.createBufferSource()
    source.buffer = buffer
    source.connect(audioCtx.destination)
    source.start()
  }).catch(() => {
    console.log('fail')
  })
}

play()
```
