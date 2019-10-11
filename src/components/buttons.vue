<!-- <template>
  <div id="container">
    <div class="button" v-for="(site) in websites" :key="site.id">
      <button v-bind:class="tag.name" v-for="(tag, index) in site.tags" :key="index">{{ tag.name }}</button>
    </div>
  </div>
</template> -->

<!-- <script>
// import { EventBus } from "../event-bus.js";

// export default {
//   name: "Buttons",
//   // template: "#card",
//   // props: ["name", "url"],
//   data() {
//     return {
//       websites: [
//         {
//           id: null,
//           name: null,
//           url: null,
//           description: null,
//           tags: null
//         }
//       ]
//     };
//   },
//   created() {
//     // Using the server bus
//     EventBus.$on("tags", websites => {
//       this.websites = websites;
//       console.log(websites[0]);
//     });
//   }
// };
// </script> -->

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- <style scoped>
* {
  box-sizing: border-box;
}

#container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style> -->