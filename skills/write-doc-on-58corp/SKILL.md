---
name: write-doc-on-58corp
description: 在 docs.58corp.com 的指定空间（默认"我的空间"）新建并发布一篇文档。
argument-hint: [文档标题] [文档正文内容] [目标空间，默认我的空间]
---

# Skill: 在美事文档写文章

## 步骤

### 1. 打开 docs.58corp.com

```
导航到：https://docs.58corp.com
```

若页面跳转到登录页（URL 含 `passport.58corp.com`），则**通知用户登录**，等待用户确认后继续。

---

### 2. 进入目标空间

登录后会进入工作台（`#/workbench`）。

- 默认目标为"我的空间"：点击左侧常用空间列表中的"我的空间"listitem
- 该操作通常会在新 tab 打开个人空间页面，需用 `browser_tabs` select 切换到新 tab

---

### 3. 新建文档

1. 点击顶部"新建"按钮（`button " 新建"`）
2. 在弹出菜单中点击"新建文档"listitem
3. 弹出"新建到"对话框，确认目标空间正确后点击"确定"
4. 编辑器会在**新 tab** 中打开，用 `browser_tabs` select 切换到该 tab

---

### 4. 填写标题和正文

1. 点击标题输入框（`textbox "请输入文档标题"`），用 `browser_type` 填入标题
2. 点击正文段落（`paragraph`），用 `browser_type` 填入正文内容

> 注意：`browser_type` 需要同时传 `ref` 和 `element` 参数。

---

### 5. 发布文档

点击右上角"发布"按钮（`button "发布"`）。

发布成功后页面会：
- 跳转到文档阅读页（URL 从 `#/editor/...` 变为 `#/space/...`）
- 出现"保存成功"提示

---

## 注意事项

1. **新建文档和进入空间都会开新 tab**，每次操作后要检查 tab 列表并用 `browser_tabs select` 切换
2. **标题填写后文档 tab 标题会同步更新**，可用来确认标题已生效
3. **`browser_type` 要求传 `ref` 和 `element`**，否则报参数错误
4. **不要在"已经保存到云端"状态就停止**，必须点"发布"才算正式发布
