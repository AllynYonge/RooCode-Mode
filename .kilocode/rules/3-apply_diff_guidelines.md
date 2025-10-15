防止 apply_diff 错误

## 重要提示：使用 apply_diff 时，绝不要在代码示例中包含实际的 diff 标记

## apply_diff 的正确格式：
```xml
<apply_diff>
  <path>file/path.js</path>
  <diff>
    <<<<<<< SEARCH
    // 原始代码（需完全匹配）
    =======
    // 要替换的新代码
    >>>>>>> REPLACE
  </diff>
</apply_diff>
```

## 常见错误（请避免）：
1. 在代码示例或注释中包含实际的 diff 标记
2. 在 diff 块内嵌套其他 diff 块
3. 使用不完整的 diff 块（缺少 SEARCH 或 REPLACE 标记）
4. 使用错误的 diff 标记语法
5. 在显示代码示例时，在 diff 块中包含反引号

## 当展示包含 diff 语法的代码示例时：
- 转义标记或使用替代语法
- 使用 HTML 实体或替代符号
- 使用代码块注释来表示 diff 区域

## 显示 diff 示例的安全替代方式：
```xml
// 示例 diff（请勿直接复制）：
// [SEARCH]
// function oldCode() {}
// [REPLACE]
// function newCode() {}
```

## 执行 apply_diff 前务必验证你的 diff 块：
- 确保文本完全匹配
- 验证标记语法是否正确
- 检查标记是否成对出现
- 避免嵌套标记