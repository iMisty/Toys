<template>
  <div id="app">
    <h1>百度体生成器</h1>
    <label class="label">
      <input type="text" v-model="title" class="input" />
      <input type="text" v-model="event" class="input" />
    </label>
    <button type="button" @click="changeBoard">生成</button>
    <div class="tips">
      <h3>单击文本可复制</h3>
    </div>
    <div
      class="successed"
      v-if="board"
      @click="test($event)"
      v-clipboard:copy="message"
      v-clipboard:success="onCopy"
    >
      <p class="message">
        {{title}}{{event}}是怎么回事呢？{{title}}{{event}}相信大家都很熟悉， 但是{{title}}{{event}}是怎么回事呢？下面就让小编带大家一起了解吧。
        <br />
        {{title}}{{event}}，其实就是{{title}}{{event}}了。那么{{title}}为什么会{{event}}呢，相信大家都很好奇是怎么回事。大家可能会感到很惊讶，{{title}}怎么会{{event}}呢？但事实就是这样，小编也感到非常惊讶。
        <br />
        那么这就是关于{{title}}{{event}}的事情了，大家有没有觉得很神奇呢？看了今天的内容，大家有什么想法呢？欢迎在评论区告诉小编一起讨论哦
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      title: "百度",
      event: "被约谈",
      board: false,
      message: ""
    };
  },
  methods: {
    changeBoard() {
      this.board = true;
    },
    test(e) {
      this.board = true;
      console.log(e.target.innerHTML);
      this.message = e.target.innerHTML;
      this.message = this.message.replace(/<[^>]*>|/g, "");
    },
    onCopy(e) {
      alert("复制成功", e.text);
    }
  }
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
input {
  font-size: 1.2rem;
  padding: 4px;
  margin: 4px;
  border: none;
  border-bottom: 2px solid #000;
  text-align: center;
}
input:focus {
  outline: none;
}
button {
  font-size: 1.2rem;
  margin: 0 auto;
  background: none;
  padding: 4px 16px;
  border: 1px solid #333;
  @media screen and (max-width: 480px){
    display: block;
    margin-top: 12px;
  }
}
.message {
  max-width: 384px;
  padding: 0 16px;
  text-align: justify;
  margin: 0 auto;
}
</style>
