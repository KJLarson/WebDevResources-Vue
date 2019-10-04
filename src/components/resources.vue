<!-- Using https://vuejsexamples.com/a-simple-card-components-with-vue-js/ to try to make this card -->

<template>
    <div>
        <div class="card" style="width: 18rem;"  v-for="site in websites" v-bind:key="site.id">
            <div class="card-body">
                <h2 class="card-title">{{ site.name }}</h2>
                <p class="card-text">{{ site.url }}</p>
                <p>{{ site.description }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: "Resources",
  // template: "#card",
  props: ['name', 'url'],
  data() {
    return {
      websites: [
        {
          id: 1,
          name: "Open Source Guide",
          url: "https://opensource.guide/",
          description:
            "An open source markdown editor for Mac, Windows and Linux app. The intuitive and stylish note taking tool for developers.",
          tags: ["markdown", "productivity", "tool"]
        },
        {
          id: 2,
          name: "Boostnote",
          url: "https://boostnote.io/",
          description:
            "Open source software is made by people just like you. Learn how to launch and grow your project.",
          tags: ["open-source"]
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .card {
    border: gray solid 1px;
  }
</style>
