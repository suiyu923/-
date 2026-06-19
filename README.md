
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
本项目由DeepSeek AI 辅助创作完成
import torch
from transformers import AutoProcessor, AutoModelForVisionAndImageGeneration

# 加载本地Janus模型（Deepseek文生图专用）
model_name = "deepseek-ai/Janus-Pro-7B"
processor = AutoProcessor.from_pretrained(model_name)
model = AutoModelForVisionAndImageGeneration.from_pretrained(
    model_name,
    torch_dtype=torch.bfloat16,
    device_map="auto"
)

# 赐名阁绘图指令
prompt = """写实摄影，江南双层古建赐名阁，青绿色琉璃瓦飞檐楼阁，木匾书写赐名阁，古松前景，柔和日光，8K，古风实景，1280×960"""

# 处理输入、生成图像
inputs = processor(text=prompt, return_tensors="pt").to("cuda", torch.bfloat16)
with torch.no_grad():
    output_imgs = model.generate(
        **inputs,
        height=960,
        width=1280,
        num_inference_steps=28,
        guidance_scale=7.5
    )

# 保存图片
img = processor.decode_image(output_imgs[0])
img.save("赐名阁_古风生成图.jpg")
print("图片已保存为 赐名阁_古风生成图.jpg")

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

