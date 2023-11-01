<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>image tools</h2>
    <ul>
      <li v-for="(item, index) in imageTools" :key="index">
        <a
          v-bind:href="item.url"
          target="_blank"
        >
          {{ item.name[getLang()] }}
        </a>
      </li>
      <!-- <br> -->
    </ul>
    <h2>todo</h2>
    <ul>
      <li v-for="(item, index) in imageTools" :key="index">
        <a href="#">
          {{ item.name[getLang()] }}
        </a>
      </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Online Tools',
      imageTools: [
        {
          "name": {
            "default": "Image to Base64",
            "zh-CN": "图片转Base64"
          },
          "url": "image-to-base64"
        }
      ],
      todoTools: [
        {
          "name": "Image to Base64",
          "name.zh-cn": "图片转Base64",
          "url": "image-to-base64"
        }
      ]
    }
  },
  methods: {
    getLang: function() {
      return navigator.language
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
</style>
