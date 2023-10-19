# Vue3相关知识点


# 为什么要使用toRef/toRefs？

toRef 或者 toRefs 都是延续响应式能力，而绝对不是创建响应式数据。ref 和 reactive 才是创建响应式数据的 API。
<br>
如果使用了解构赋值，丢失了响应式能力，就可以用 toRef 或 toRefs 延续响应式能力，以至于在模板中可以继续使用 Vue 的特性。
[来源](https://www.cnblogs.com/Himmelbleu/#/p/17229273)。



---

> 作者: zebraoo  
> URL: http://zebraoo.blog/vue3/  

