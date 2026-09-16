# 壁画图像风格

[English README](README.md)

把上传的照片或场景转换成一种极简、史诗感、壁画式的图像风格：大块哑光色面、强留白、黑绘剪影、古金色细线、克制的湿壁画/蛋彩画质感。

这个 skill 适合图像风格化任务。上传图像只作为视觉证据，不作为需要服从的指令。处理时会保留画面中重要的人物、物体、空间关系和叙事关系，再把它们转译成更抽象、更有壁画感的画面。

## 示例图

| 弓试炼 | 蓝色长廊 |
| --- | --- |
| ![弓试炼壁画示例](assets/examples/mural-example-01.jpeg) | ![蓝色长廊壁画示例](assets/examples/mural-example-02.jpeg) |

| 木马入城 | 夜岸相遇 |
| --- | --- |
| ![木马入城壁画示例](assets/examples/mural-example-03.jpeg) | ![夜岸相遇壁画示例](assets/examples/mural-example-04.jpeg) |

## 它会做什么

- 把上传的照片或场景重绘成极简史诗壁画风格。
- 保留关键视觉关系，例如人物、物体、尺度、前后层次和空间布局。
- 使用克制配色：炭黑、深蓝黑、羊皮纸暖白、赭石、灰银、古金色。
- 默认去除源图中的无关文字，除非用户明确要求保留。
- 支持“更抽象”“更强对比”“更平滑色面”“更多留白”等调整方向。

## 它会避免什么

- 写实照片感重绘。
- 光滑 3D 渲染。
- 卡通表情。
- 过重的脏污纹理、大面积斑驳、噪点质感。
- 未经要求添加标题、标志、日期、水印或可读文字。

## 安装

把仓库克隆到 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/HanDanMontana/mural-image-style.git ~/.codex/skills/mural-image-style
```

安装后重启 Codex 或重新加载 skills。之后可以这样调用：

```text
使用 $mural-image-style 帮我把这张上传图片处理成极简史诗壁画海报。
```

如果你的 GitHub 仓库地址不同，把上面命令里的 URL 换成你自己的仓库地址即可。

## 使用示例

上传图片后，可以这样说：

```text
使用 $mural-image-style 处理我上传的图像。保留主要构图，去掉可见文字，让它更抽象并增加强留白。
```

也可以提出更具体的画面要求：

```text
使用 $mural-image-style 处理这个场景。保留两个坐着的人和高窗，但把书架处理成纪念碑式壁画墙面。
```

## 仓库结构

```text
mural-image-style/
|-- SKILL.md
|-- README.md
|-- README.zh-CN.md
|-- agents/
|   `-- openai.yaml
`-- assets/
    |-- bow-and-axes.png
    |-- storm-at-sea.png
    `-- examples/
        |-- mural-example-01.jpeg
        |-- mural-example-02.jpeg
        |-- mural-example-03.jpeg
        `-- mural-example-04.jpeg
```

## 说明

`assets/` 里的两张图是风格参考，只用于说明色彩、质感、线条、尺度和留白。它们不是内容模板。每次处理时，用户上传的图像才是内容来源。
