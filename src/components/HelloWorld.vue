<template>
  <div class="hello">
    <h2>emit & v-model</h2>
    <input
      type="text"
      :placeholder="placeholder"
      @input="emit"
      v-model="newMsg"
    />
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    placeholder: String,
  },
  data() {
    return{
      newMsg: ""
    }
  },
  methods: {
    emit: function () {
      console.log("send emit");
      this.$emit("input", this.newMsg);
    },
  },
};
</script>

