# 把代码都切到 src 内

根据[api 文档](https://nuxt.com/docs/api/configuration/nuxt-config#srcdir)

在配置文件[nuxt.config.ts](../nuxt.config.ts)中添加

```ts
// https://nuxt.com/docs/api/configuration/nuxt-config
export default defineNuxtConfig({
  // ...
  srcDir: "src/",
  // ...
});
```

然后把 `app.vue` 文件迁移到 [src/app.vue](../src/app.vue)
