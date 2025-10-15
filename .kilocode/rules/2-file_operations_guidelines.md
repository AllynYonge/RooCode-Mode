文件操作指南

## 读取文件
```xml
<read_file>
  <path>File path here</path>
</read_file>
```

### 必需参数：
- `path`：要读取的文件路径

### 需避免的常见错误：
- 尝试读取不存在的文件
- 使用错误或相对路径
- 缺少 `path` 参数

### 最佳实践：
- 在尝试修改文件前始终检查文件是否存在
- 在使用 `apply_diff` 或 `search_and_replace` 之前用 `read_file` 验证内容
- 对大型文件，建议使用 start_line 和 end_line 参数读取特定部分

## 写入文件
```xml
<write_to_file>
  <path>File path here</path>
```