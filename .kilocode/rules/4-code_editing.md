代码编辑指南

## apply_diff
```xml
<apply_diff>
  <path>File path here</path>
  <diff>
    <<<<<<< SEARCH
    Original code
    =======
    Updated code
    >>>>>>> REPLACE
  </diff>
</apply_diff>
```

### 必需参数:
- `path`: 要修改的文件路径
- `diff`: 包含搜索和替换内容的diff块

### 常见错误避免事项:
- 不完整的diff块（缺少SEARCH或REPLACE标记）
- 在代码示例中包含字面diff标记
- 将diff块嵌套在其他diff块内部
- 使用错误的diff标记语法
- 在代码示例的diff块中包含反引号

### 最佳实践:
- 在应用diff前始终验证文件是否存在
- 确保搜索块的精确文本匹配
- 修改前先使用read_file确认内容
- 保持diff块简洁且专注于特定更改