在 TypeScript 中，可以使用正则表达式来将小驼峰命名（camelCase）转换为下划线命名（snake_case）。以下是一个示例函数，演示如何实现这一转换：

```typescript
function camelToSnake(camelCase: string): string {
    return camelCase.replace(/([A-Z])/g, '_$1').toLowerCase();
}

// 示例用法
const userToken = "userToken";
const snakeCase = camelToSnake(userToken);
console.log(snakeCase); // 输出: user_token
```

### 代码解释：
1. **正则表达式**：`/([A-Z])/g` 匹配所有大写字母。
2. **替换**：`'_$1'` 将匹配到的大写字母前加上下划线。
3. **转换为小写**：使用 `toLowerCase()` 方法将整个字符串转换为小写。

你可以将这个函数应用于任何小驼峰命名的字符串，以获得对应的下划线命名字符串。
