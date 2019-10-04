<!-- Using https://vuejsexamples.com/a-simple-card-components-with-vue-js/ to try to make this card -->

<template>
  <div>
    <div class="card" v-for="site in websites" v-bind:key="site.id">
      <div class="card-body">
        <h2 class="card-title">{{ site.name }}</h2>
        <p>{{ site.description }}</p>
        <p>
          Go to
          <a v-bind:href="site.url">{{ site.name }}</a>
        </p>
        <ul class="tags">
          <li v-for="tag in site.tags">{{ tag.name }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Resources",
  // template: "#card",
  // props: ["name", "url"],
  data() {
    return {
      websites: [
        {
          id: 1,
          name: "Boostnote",
          url: "https://boostnote.io/",
          description:
            "Open source software is made by people just like you. Learn how to launch and grow your project.",
          tags: [{ name: "open-source" }]
        },
        {
          id: 2,
          name: "Linked Ideas",
          url: "http://fespinoza.github.io/LinkedIdeas/",
          description: "A macOS/iOS apps to treat ideas as links of concepts.",
          tags: [{ name: "productivity" }, { name: "tool" }]
        },
        {
          id: 3,
          name: "Open Source Guide",
          url: "https://opensource.guide/",
          description:
            "An open source markdown editor for Mac, Windows and Linux app. The intuitive and stylish note taking tool for developers.",
          tags: [
            { name: "markdown" },
            { name: "productivity" },
            { name: "tool" }
          ]
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  box-sizing: border-box;
}

.card {
  border: gray solid 1px;
  margin: 5px;
  text-align: center;
  background-color: lightgray;
  padding: 8px;
}

.tags {
  list-style: none;
  display: flex;
  justify-content: center;
}

.tags li {
  padding: 5px;
  margin: 0 5px;
  border: gray solid 1px;
  background-color: lightgoldenrodyellow;
}
</style>
