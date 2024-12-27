# Item-Resurrection-CS3331-FinalProject
# 物品复活软件（Items-Revival）

## 项目概述
大学生们往往有些物品舍不得丢掉，但不处理又占用太多空间。本软件旨在帮助这些物品找到新的用途，或者帮助拥有者更好地管理这些物品。通过使用物品“复活”软件，用户可以添加、管理和查找物品，记录它们的详细信息，方便日后的利用或者转赠。

物品复活系统（Items-revival)是一个基于 Python 和 Tkinter 开发的桌面应用程序，支持对物品的管理，包括添加、编辑、删除、恢复、以及从回收站永久删除等功能。项目使用 SQLite 数据库来存储物品数据，并提供友好的图形用户界面（GUI）进行交互。

为CS3331软件工程（2024-2025-1）课程的课程项目。

---

## 功能概述

### 1. **物品管理**
- 添加新物品，支持填写以下信息：
  - 名称
  - 类别（食品、书籍、工具）
  - 描述
  - 地址
  - 联系人信息（手机、邮箱）
  - 扩展属性（根据类别动态生成，如食品的保质期、书籍的作者等）
- 搜索物品：
  - 按类别搜索。
  - 支持模糊关键词搜索（名称、描述、联系人信息等）。
- 编辑物品：
  - 支持加载选中物品到编辑框并修改。
  - 避免与现有物品名称和类别重复的冲突。
- 删除物品：
  - 删除后物品会被移动到“回收站”，用户可以选择恢复或永久删除。

### 2. **回收站管理**
- 查看所有被删除的物品。
- 恢复物品：
  - 支持将物品从回收站恢复到主物品列表。
  - 如果存在名称和类别冲突，可选择替换或放弃恢复。
- 永久删除物品：
  - 不可恢复，操作需用户确认。

### 3. **动态扩展属性**
根据物品类别，系统会动态生成扩展属性字段：
- **食品**：
  - 保质期
  - 数量
- **书籍**：
  - 作者
  - 出版社
- **工具**：
  - 品牌
  - 型号

---

## 技术栈

- **语言**：Python
- **界面**：Tkinter
- **数据库**：SQLite3
- **数据格式**：JSON（存储扩展属性）
