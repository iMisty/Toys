<template>
  <div class="successed">
    <p>{{title}}{{event}}是怎么回事呢？{{title}}{{event}}相信大家都很熟悉， 但是{{title}}{{event}}是怎么回事呢？下面就让小编带大家一起了解吧。</p>
    <p>{{title}}{{event}}，其实就是{{title}}{{event}}了。那么{{title}}为什么会{{event}}呢，相信大家都很好奇是怎么回事。大家可能会感到很惊讶，{{title}}怎么会{{event}}呢？但事实就是这样，小编也感到非常惊讶。</p>
    <p>那么这就是关于{{title}}{{event}}的事情了，大家有没有觉得很神奇呢？看了今天的内容，大家有什么想法呢？欢迎在评论区告诉小编一起讨论哦</p>
  </div>
</template>

<script>
export default {
  //组件
  components: {},
  //静态
  props: {
    title: {
      type: String,
      default: ""
    },
    event: {
      type: String,
      default: ""
    }
  },
  //保存数据用
  data() {
    return {};
  },
  //对象内部的属性监听，也叫深度监听
  watch: {},
  //属性的结果会被缓存，除非依赖的响应式属性变化才会重新计算。主要当作属性来使用；
  computed: {},
  //方法表示一个具体的操作，主要书写业务逻辑；
  methods: {},
  //请求数据
  created() {},
  mounted() {}
};
</script>

<style lang='less' scoped>
</style>