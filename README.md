
<!--
╔══════════════════════════════════════════════════════════════════════╗
║  DreamSeed 种梦计划 — AI创造者大赛  官方 README 模板                ║
║                                                                      ║
║  使用说明：                                                          ║
║  1. 将本模板放在参赛仓库根目录 README.md 的顶部                       ║
║  2. 头图使用 DreamField 官方公开活动图片地址                         ║
║  3. 请保留 DREAMFIELD_README_HEADER_START / END 标识                 ║
║  4. 分割线以下供创作者自由编写项目内容                               ║
╚══════════════════════════════════════════════════════════════════════╝
-->

<!-- DREAMFIELD_README_HEADER_START -->

<p align="center">
  <a href="https://www.dreamfield.top">
    <img src="https://www.dreamfield.top/dream-field/contest-readme/assets/dreamseed-readme-banner.png" alt="DreamSeed 种梦计划参赛作品" width="100%" />
  </a>
</p>

<!-- DREAMFIELD_README_HEADER_END -->
## 🙏 鸣谢
本项目全程由 Deepseek AI 辅助完成开发工作；特别感谢 Dreamfield 对本计划的大力宣传与推广支持。
 
📚🏠赐名阁🏠📚

<img width="1706" height="1280" alt="ceab7ba6e71c14954451bc1f7e8bace5" src="https://github.com/user-attachments/assets/b545f663-550c-4fb4-8b8a-9b85bbe579f4" />

## 使用方法

```
var SearchSong = require('./index');

SearchSong({
  text : '张',          // 需要查找的字或者词语
  debug: { num: 2 },    //debug 选项仅供调试，正式使用的时候可以删掉
  nolastWord : true     // true 了之后，会过滤掉以这个字结尾的结果
}).then(function(result){
    console.log(result);
});
```

