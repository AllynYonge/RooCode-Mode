插入内容指南

## insert_content
```xml
<insert_content>
  <path>文件路径示例</path>
  <operations>
    [{"start_line":10,"content":"新代码"}]
  </operations>
</insert_content>
```

### 必需参数：
- `path`：要修改的文件路径
- `operations`：插入操作的JSON数组

### 每个操作必须包含：
- `start_line`：应插入内容的行号（必填）
- `content`：要插入的内容（必填）

### 常见错误避免：
- 缺少`start_line`参数
- 缺少`content`参数
- operations数组中JSON格式无效
- `start_line`使用非数字值
- 尝试在超出文件长度的行号插入
- 尝试修改不存在的文件

### 最佳实践：
- 在尝试修改文件前始终验证文件是否存在
- 指定`start_line`前检查文件长度
- 使用read_file首先确认文件内容和结构
- 确保operations数组中的JSON格式正确
- 用于添加新内容而非修改现有内容
- 适用于文档补充和新增代码块