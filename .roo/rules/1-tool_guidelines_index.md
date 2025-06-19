# 工具使用指南索引

为防止在使用工具时出现常见错误，请参考以下详细指南：

## 文件操作
- [文件操作指南](.roo/rules-code/file_operations.md) - 关于 read_file、write_to_file 和 list_files 的指南

## 代码编辑
- [代码编辑指南](.roo/rules-code/code_editing.md) - 关于 apply_diff 的指南
- [查找与替换指南](.roo/rules-code/search_replace.md) - 关于 search_and_replace 的指南
- [插入内容指南](.roo/rules-code/insert_content.md) - 关于 insert_content 的指南

## 常见错误预防

- [apply_diff 错误预防](.roo/rules-code/apply_diff_guidelines.md) - 预防 apply_diff 错误的具体指南

## 需要记住的要点：

1. 始终为每个工具包含所有必需的参数
2. 在尝试修改之前，验证文件是否存在
3. 对于 apply_diff，不要在代码示例中包含字面差异标记
4. 对于 search_and_replace，始终包含搜索和替换参数
5. 对于 write_to_file，始终包含 line_count 参数
6. 对于 insert_content，始终在操作数组中包含有效的 start_line 和 content