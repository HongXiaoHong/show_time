# show_time

个人作品集网站展示

## 搭建一个 vuetify

[Get started with Vuetify 3 — Vuetify (vuetifyjs.com)](https://vuetifyjs.com/en/getting-started/installation/)



学习 vuetify 可以上 [Vuetify — Playground --- Vuetify — 游乐场 (vuetifyjs.com)](https://play.vuetifyjs.com/#eNqVkd1OAjEQhV+l6TXdJoLGEDT4HJSLsh2w2L+0ZQUJ7+60CNmABrzbzsz5zpnZ2Z6+hdB0G6BjOslgg5EZXoUjZKJ0R1ojU3oRVLGlgS2RRq8ca8FliGS9SVkvdywF2QKT0W+cErRqUd0x2cksI2m98RERIWor405QkvQXYGHLkpXGnCWEDB9+xPykxtZfvAStd6oSz4DR8z8A2i19P42RcQU92NPoF1h54mHwa8LP56IDarT7SM06eYeH3Jc5QduUBB2T2REj6HvOIY05b5XDSQVGd7FxkLkLluMvKNecDpth84gWKZ9KGGyRmgorpLlwBzTUNviYmZXhwvXYqM61UmpIKu8bEaY4xuPGZW2BKW9rltExS6/cQLJsEf1ngogQQQc9mxL4Dqtb26LFFZqjXweRRXAKIsR7N7qQ9be6aF1tVtwP5d6HAa0yPHyNTOffuggR+A==)



环境: 升级 node 可以使用 nvm

| 软件   | 版本       |
| ---- | -------- |
| npm  | 9.8.0    |
| node | v18.16.1 |

```bash
npm create vuetify
```

```bash

success Installed "create-vuetify@x.x.x" with binaries:
    - create-vuetify

? Project name: ❯ vuetify-project // the folder to generate your application
? Use TypeScript?: ❯ No / Yes
? Would you like to install dependencies with yarn, npm, or pnpm?:
  ❯ yarn
    npm
    pnpm
    none
```

## Project setup

```
# yarn
yarn

# npm
npm install

# pnpm
pnpm install
```

### Compiles and hot-reloads for development

```
# yarn
yarn dev

# npm
npm run dev

# pnpm
pnpm dev
```

### Compiles and minifies for production

```
# yarn
yarn build

# npm
npm run build

# pnpm
pnpm build
```

### Lints and fixes files

```
# yarn
yarn lint

# npm
npm run lint

# pnpm
pnpm lint
```

### Customize configuration

See [Configuration Reference](https://vitejs.dev/config/).





```bash
# 测试
D:\app\code\nginx-1.24.0>start nginx -t -c ./conf/nginx_show_time.conf
nginx: the configuration file ./conf/nginx_show_time.conf syntax is ok
nginx: configuration file ./conf/nginx_show_time.conf test is successful
# 开启
D:\app\code\nginx-1.24.0>start nginx -c ./conf/nginx_show_time.conf
# 退出
D:\app\code\nginx-1.24.0>nginx -s quit
```

### 总结
#### 组件
##### chips | 标签
使用 chips 给项目描述增加技能标签
```vue
<template>
  <div class="text-center">
    <v-chip
      class="ma-2"
      color="indigo"
      text-color="white"
      prepend-icon="mdi-account-circle"
    >
      Mike
    </v-chip>

    <v-chip
      class="ma-2"
      color="orange"
      text-color="white"
      append-icon="mdi-star"
    >
      Premium
    </v-chip>

    <v-chip
      class="ma-2"
      color="primary"
      text-color="white"
      append-icon="mdi-cake-variant"
    >
      1 Year
    </v-chip>

    <v-chip
      class="ma-2"
      color="green"
      text-color="white"
    >
      <template v-slot:prepend>
        <v-avatar
          class="green-darken-4"
        >
          1
        </v-avatar>
      </template>
      Years
    </v-chip>

    <v-chip
      class="ma-2"
      closable
      color="teal"
      text-color="white"
      prepend-icon="mdi-checkbox-marked-circle"
      :model-value="true"
    >
      Confirmed
    </v-chip>

    <v-chip
      class="ma-2"
      closable
      color="teal"
      text-color="white"
      close-icon="mdi-delete"
      prepend-icon="mdi-checkbox-marked-circle"
      :model-value="true"
    >
      Confirmed
    </v-chip>
  </div>
</template>
```
![chips标签](https://raw.githubusercontent.com/HongXiaoHong/images/main/picture/msedge_tRGk9nIKrk.png)
#### 布局

##### flex | 弹性布局
https://vuetifyjs.com/en/styles/flex/