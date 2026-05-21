
---

# 一、高频必用
## 1. 带固定锚点的标题标签（解决目录跳转）
```html
<!-- 一级标题，对应 Markdown 的 # -->
<h1 id="chapter-1">第一章 函数</h1>

<!-- 二级标题，对应 Markdown 的 ## -->
<h2 id="section-1-periodicity">1. 周期性</h2>

<!-- 三级标题，对应 Markdown 的 ### -->
<h3 id="subsection-1-1">1.1 周期信号特点</h3>
```
- 用法：`id="你自己取的唯一名字"`，目录里写 `[文字](#你取的名字)` 就能跳。
- 优势：**永远不会因为改标题文字导致跳转失效**。

---

# 二、排版美化（让笔记更好看）
## 2. 文本样式标签
```html
<!-- 加粗 -->
<b>重点内容</b>

<!-- 斜体 -->
<i>补充说明</i>

<!-- 删除线 -->
<s>过时的内容</s>

<!-- 上标/下标（写公式/单位超好用） -->
x<sup>2</sup>  <!-- x² -->
CO<sub>2</sub> <!-- CO₂ -->
```

## 3. 带颜色/大小的文本（给笔记加重点）
```html
<!-- 红色重点 -->
<span style="color: red;">❌ 易错点</span>

<!-- 灰色小字说明 -->
<span style="color: #666; font-size: 0.8em;">（嵌入式场景：PWM 周期）</span>
```

## 4. 换行与分隔
```html
<!-- 强制换行（比 Markdown 两个空格更稳） -->
<br>

<!-- 水平分隔线（和 --- 效果一样，但可以自定义样式） -->
<hr style="border: 1px solid #eee;">
```

---

# 三、链接与跳转（笔记必备）
## 5. 跳转链接（除了目录，还能跳外部链接）
```html
<!-- 跳转到笔记内的锚点 -->
<a href="#section-1-periodicity">返回周期性小节</a>

<!-- 跳转到外部链接 -->
<a href="https://github.com">访问 GitHub</a>

<!-- 打开新标签页的外部链接 -->
<a href="https://github.com" target="_blank">访问 GitHub（新标签页）</a>
```

---

# 四、暂时不用管的标签（避免混淆）
这些在 GitHub Markdown 里**用不上或不生效**的标签，不用学：
- `<html>` / `<body>`：完整 HTML 文档的结构标签，GitHub 会自动生成，写了也没用。
- `<head>` / `<title>`：网页头部信息，GitHub 会自动设置页面标题，不用写。
- `<style>`：自定义 CSS 样式，GitHub Markdown 不支持，写了也不会生效。

---

# 五、「笔记通用模板」（直接复制就能用）
```markdown
# 目录
- [第一章 函数](#chapter-1)
  - [1. 周期性](#section-1-periodicity)
  - [2. 奇偶性判断](#section-1-parity)

---

<h1 id="chapter-1">第一章 函数</h1>

<h2 id="section-1-periodicity">
  1. 周期性
  <span style="color: #666; font-size: 0.8em;">（复合函数周期判断）</span>
</h2>
内容：若存在 $f(x+T)=f(x)$，则最小正数 $T$ 为最小正周期。
<br>
嵌入式场景：时钟、PWM 波的周期计算。

🔝 <a href="#目录">返回目录</a>

---

<h2 id="section-1-parity">2. 奇偶性判断</h2>
口诀：内奇则奇，内偶则偶。
<br>
例：$y=\sin(x^2)$：内层偶 → 整体偶
<span style="color: red;">❌ 易错：直接看外层奇偶，忽略内层</span>

🔝 <a href="#目录">返回目录</a>
```
