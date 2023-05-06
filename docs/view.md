# 组件，页面和 layout

组件和页面都可以是按文件夹结构自动构建

创建 [src/components/AppTest.vue](../src/components/AppTest.vue)

```vue
<template>
  <div>App test components <slot /></div>
</template>
```

然后把 `src/app.vue` 调整到 [src/pages/index.vue](../src/pages/index.vue) 并修改为

```vue
<template>
  <div>
    <h1>Welcome to the homepage</h1>
    <AppTest> This is an auto-imported component </AppTest>

    <a href="/about">go to about page </a>
  </div>
</template>
```

这样就可以组件自动加载了

再创建 [src/pages/about.vue](../src/pages/about.vue)

```vue
<template>
  <section>
    <p>This page will be displayed at the /about route.</p>

    <a href="/">go back index page </a>
  </section>
</template>
```

可以启动一下看看效果～

这里 pages 下的文件就会自动构建出两个路由，一个是 `/` 和 `/about`

更多关于 `router` 的配置请看 [文档](https://nuxt.com/docs/getting-started/routing)

## layout

如果想每个页面都有一样的母版，可以创建

创建 [src/components/AppHeader.vue](../src/components/AppHeader.vue)

```vue
<template>
  <div>App header</div>
</template>
```

创建 [src/components/AppFooter.vue](../src/components/AppFooter.vue)

```vue
<template>
  <div>App footer</div>
</template>
```

创建 [src/layouts/default.vue](../src/layouts/default.vue)

```vue
<template>
  <div>
    <AppHeader />
    <slot />
    <AppFooter />
  </div>
</template>
```
