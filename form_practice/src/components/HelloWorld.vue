<template>
  <div class="hello">
    <form @submit.prevent="sendSubmit">
      <input type="text" v-model="event.name">
      <input type="text" v-model="event.lastName">
      <button type="submit" @click="invokes">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      event: {
        name: "",
        lastName: "",
      },
    };
  },
  methods:{
    eventInput1(value){
      console.log(value);
    },
    invokes(){
      console.log(this.event.name);
    }
  }
};
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
</style>
