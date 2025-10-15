查找与替换指南

## search_and_replace
```xml
<search_and_replace>
  <path>文件路径</path>
  <operations>
    [{"search":"旧文本","replace":"新文本","use_regex":true}]
  </operations>
</search_and_replace>
```

### 必需参数：
- `path`：要修改的文件路径
- `operations`：查找与替换操作的 JSON 数组

### 每个操作必须包含：
- `search`：要查找的文本（必需）
- `replace`：要替换的新文本（必需）
- `use_regex`：布尔值，指示是否使用正则表达式（可选，默认为 false）

### 常见应避免的错误：
- 缺少 `search` 参数
- 缺少 `replace` 参数
- 操作数组中存在无效的 JSON 格式
- 尝试修改不存在的文件
- 当 `use_regex` 为 true 时，正则表达式格式不正确

### 最佳实践：
- 始终同时包含 `search` 和 `replace` 参数
- 在尝试修改之前确认文件是否存在
- 对于复杂更改，请改用 `apply_diff`
- 在使用前单独测试正则表达式模式
- 在正则表达式中转义特殊字符