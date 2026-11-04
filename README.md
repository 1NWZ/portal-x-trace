# PORTAL-X TRACE

为图片和视频叠加追踪框、证据标签、科学网格、监控界面、故障和胶片颗粒的本地浏览器工具及 Agent Skill。

## 静态图片输出规则

静态图片输入默认交付单张静态 PNG，原照片保持静止，叠加效果定格在单帧。只有明确要求动画或视频时才录制 WebM。预览中的动态效果不代表最终 PNG 会动；原始文件不会被覆盖。

此规则已写入 SKILL.md。网页工具保留手动 PNG 导出和 WebM 录制功能。

## 使用方式

将整个仓库下载为技能目录，保留 SKILL.md 与 assets/ 的相对位置。也可以直接启动配套网页：

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory assets/webapp
```

在浏览器打开 http://127.0.0.1:8000，上传本地图片或视频，选择风格、比例及配色，点击 Export Frame (.PNG) 导出静态图。明确需要动态视频时使用 REC Video (.WebM)。推荐使用 Chromium 浏览器进行视频录制。

## 风格

- Evidence Tree：档案证据标签与连线。
- Red Machine：警报色块与追踪框。
- Biotech Grid：科学网格与坐标。
- Surveillance：监控标记与目标编号。

媒体处理在本地浏览器完成；网页无需构建、外部依赖或 CDN。追踪效果为视觉模拟，不适用于精密测量。

## 来源与修改

基于 RedSkill 分发的 portalxtrace 1.0.0。此版本整理了技能目录，并更新静态图片默认输出 PNG 的技能规则。网页代码保持原样，安装器本地元数据不包含在仓库中。

## License

MIT License，详见 LICENSE。
