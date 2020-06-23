<template>
  <div class="hello">
    <h1 @click="handlEvent">{{ msg }}</h1>

    <textarea  v-model="textarea" ></textarea>
    <p>输入的内容：</p>
    <p class="pre"> {{ textarea }}</p>

    <input type="radio" v-model="picked" value="html" id="html">
    <label for="html">HTML</label>
    <br>
    <input type="radio" v-model="picked" value="js" id="js">
    <label for="js">JS</label>
    <br>
    <input type="radio" v-model="picked" value="css" id="css">
    <label for="css">CSS</label>
    <br>
    <p>选择的选项是： {{ picked }}</p>

    <select v-model="selected" multiple>
      <option>html</option>
      <option value="js">javascript</option>
      <option>css</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      textarea:'textarea',
      picked:'js',
      selected:['html','css'],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.pre{white-space: pre;}
</style>
