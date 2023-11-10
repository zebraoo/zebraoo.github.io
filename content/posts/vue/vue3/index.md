+++
title = 'Vue3相关知识点'
date = 2023-10-19
tags= ['Vue3']
+++

# 为什么要使用toRef/toRefs？

toRef 或者 toRefs 都是延续响应式能力，而绝对不是创建响应式数据。ref 和 reactive 才是创建响应式数据的 API。
<br>
如果使用了解构赋值，丢失了响应式能力，就可以用 toRef 或 toRefs 延续响应式能力，以至于在模板中可以继续使用 Vue 的特性。
[来源](https://www.cnblogs.com/Himmelbleu/#/p/17229273)。

# Vue 3使用vite 2.0 动态引入加载图片 :src，解决方法超级简单


解决方法一
根据官网的提示，我找到了最简单的方法，就是在将asset 前面加上src。

<img v-if="post.welcomeScreen" :src="`/src/assets/blogPhotos/${name}.jpg`" alt="" />

解决方法二

关于第二个方法，官网说：“实际上，Vite 并不需要在开发阶段处理这些代码！在生产构建时，Vite 才会进行必要的转换保证 URL 在打包和资源哈希后仍指向正确的地址。”

因此，以下的方法开发阶段不需要了解。

首先把给src绑定一个函数，然后把需要图片名字传给函数。
[来源](https://blog.csdn.net/weixin_44717047/article/details/119846671)