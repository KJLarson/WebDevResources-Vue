<!-- Using https://vuejsexamples.com/a-simple-card-components-with-vue-js/ to try to make this card -->

<template>
  <div id="container">
    <div class="card" v-for="(site) in alphaWebsites" :key="site.id">
      <div class="card-body">
        <h2 class="card-title">{{ site.name }}</h2>
        <p>{{ site.description }}</p>
        <p>
          Go to
          <a v-bind:href="site.url">{{ site.name }}</a>
        </p>
        <ul class="tags">
          <li v-bind:class="tag.name" v-for="(tag, index) in site.tags" :key="index">{{ tag.name }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>



<script>
import { EventBus } from "../event-bus.js";

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
        },
        {
          id: 4,
          name: "Gatsby Advanced Starter",
          url: "https://github.com/Vagr9K/gatsby-advanced-starter",
          description:
            "A high performance skeleton starter for GatsbyJS that focuses on SEO/Social features/development environment.",
          tags: [{ name: "gatsby" }]
        }
      ]
    };
  },
  computed: {
    alphaWebsites: function() {
      return this.websites.slice().sort(function(a, b) {
        let nameA = a.name.toUpperCase();
        let nameB = b.name.toUpperCase();
        if (nameA < nameB) {
          return -1;
        }
        if (nameA > nameB) {
          return 1;
        }
        return 0;
      });
    }
  }
  // methods: {
  //   sendData: function() {
  //     // Send the event on a channel (websites)
  //     EventBus.$emit("tags", this.websites);
  //   }
  // }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  box-sizing: border-box;
}

#container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.card {
  border: gray solid 1px;
  margin: 5px;
  text-align: center;
  background-color: lightgray;
  padding: 8px;
  width: 45%;
}

.tags {
  list-style: none;
  display: flex;
  justify-content: center;
  width: 100%;
}

.tags li {
  padding: 5px;
  margin: 0 5px;
  border: gray solid 1px;
  background-color: lightgoldenrodyellow;
}
</style>
