# PORTAL-X TRACE

为图片和视频叠加追踪框、证据标签、科学网格、监控界面、故障和胶片颗粒的本地浏览器工具及 Agent Skill。

## 无 API 版：按请求选择输出

- **静态图请求**：使用本地网页工具，输出单张静态 PNG，保留原始文件。
- **AI 视频请求**：编写与输入照片匹配的 Seedance 图生视频提示词；有可用且已授权的模型工具或网页工作流时执行生成。静态照片也可以作为视频首帧。
- **没有可用视频模型时**：交付完整提示词和操作说明，并明确标注“尚未生成视频”。本技能不自带模型、账号或额度，也不要求配置 API 密钥或接入点。
- **输出格式**：保留模型返回的视频格式，不强制 MP4。
- **网页录制**：仅在明确要求录制本地效果预览时使用 WebM，不能代替 Seedance AI 视频生成。

详细流程见 [SKILL.md](SKILL.md) 和 [Seedance 无 API 工作流](references/seedance-no-api.md)。

## 使用方式

将整个仓库下载为技能目录，保留 SKILL.md、references/ 与 assets/ 的相对位置。也可以直接启动配套网页：

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory assets/webapp
```

在浏览器打开 http://127.0.0.1:8000，上传本地图片或视频，选择风格、比例及配色，点击 Export Frame (.PNG) 导出静态图。只有明确需要录制本地效果预览时才使用 REC Video (.WebM)。AI 视频请求按上面的 Seedance 工作流处理。

## 风格

- Evidence Tree：档案证据标签与连线。
- Red Machine：警报色块与追踪框。
- Biotech Grid：科学网格与坐标。
- Surveillance：监控标记与目标编号。

本地网页中的媒体处理在浏览器完成；网页无需构建、外部依赖或 CDN。实际使用远程 AI 模型或网页生成视频时，会向所选服务提交图片和提示词。追踪效果为视觉模拟，不适用于精密测量。

## 来源与修改

基于 RedSkill 分发的 portalxtrace 1.0.0。此版本整理了技能目录，并添加不依赖 API 配置的 Seedance 视频工作流及静态 PNG 输出规则。网页代码保持原样，安装器本地元数据不包含在仓库中。

## License

MIT License，详见 LICENSE。
