<template>
  <div class="container my-3">
    <h1>Textarea</h1>
    <div class="form-floating my-3">
      <textarea
        class="form-control"
        id="textarea"
        v-model="text"
        style="height: 50vh"
        placeholder="###"
      ></textarea>
      <label id="label" for="textarea">Enter your text here...</label>
    </div>
    <div class="containe d-flex justify-content-between">
      <div class="">
        <h4>Details...</h4>
        <p>
          No. of character : {{ text.replace(/\s+/g, " ").length }} || No. of
          words : {{ noOfWords() }}
        </p>
      </div>
      <div class="d-flex gap-0">
        <butt
          text="<img src='..\icons\backspace-icon.svg'>"
          title="Extra Space"
          content="remove extra space"
        ></butt>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Butt from "../components/Button.vue";
export default {
  name: "Home",
  methods: {
    noOfWords() {
      let text = " " + this.text.replace(/\s+/g, " ");
      let c = 0;
      for (let i = 0; i < text.length - 1; i++)
        if (text[i] == " " && text[i + 1] != " ") c++;

      return c;
    },
  },
  data() {
    return {
      text: "",
      no: 0,
    };
  },
  components: {
    Butt,
  },
};
</script>

<style scoped>
* {
  color: white;
  /* outline: auto; */
}

#textarea {
  background-color: rgba(0, 0, 0, 0.3);
  color: white;
}

.btn {
  transform: scale(0.7);
}

img {
  color: white;
}

p {
  color: gray;
}

h1 {
  text-align: center;
}
</style>
