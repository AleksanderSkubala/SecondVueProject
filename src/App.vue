<template>
  <div>
    <h1>
      Hello World!
    </h1>
    <Header />
    <ul>
      <li v-for="content in comments" class="content" :key="content.name">
        <div>
          <p> {{content.name}} </p>
          <p> {{content.content}} </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import Header from "./Header.vue";

export default {
  name: "App",
  components: {
    Header
  },
  data() {
    return {
      comments: [
        {
          name: "Olek",
          content: "My program's the best!"
        },
        {
          name: "Adam",
          content: "Yous program's the best!"
        },
        {
          name: "Roman",
          content: "You don't know nothing about progamming."
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
h1 {
  color: #bbb;
  font-family: "Helvetica";
}

.content {
  padding: 10px;
  margin: 5px;
  margin-left: none;
  background-color: silver;
  align-items: center;
  list-style: none;
  font-family: "Helvetica";
}

.content p:first-child {
  font-weight: bold;
}

.content p:last-child {
  font-size: 1.5em;
}
</style>
