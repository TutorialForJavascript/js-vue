<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <form>
      <fieldset>
        <legend>send message</legend>
        <p>
          message:
          <input type="text" name="message" v-model="msg" />
        </p>
      </fieldset>
    </form>
    <HelloWorld :msg="msg" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  data: function() {
    return {
      msg: undefined
    };
  },
  watch: {
    msg: function(val, oldVal) {
      if ((val === null) | (val === "")) {
        this.msg = undefined;
      }
    }
  },
  components: {
    HelloWorld
  }
};
</script>
