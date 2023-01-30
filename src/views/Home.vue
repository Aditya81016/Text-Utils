<template>
  <div class="container my-3">
    <h1>Textarea</h1>
    <div class="form-floating my-3">
      <textarea class="form-control" id="textarea" v-model="text" style="height: 50vh" placeholder="###"></textarea>
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
        <span @click="removeSpace">
          <butt text='<img src="src\icons\backspace-icon.svg">' title="Extra Space" content="remove extra space"></butt>
        </span>
        <span @click="copy">
          <butt text='<img src="src\icons\copy.svg">' title="Copy Text" content="copy the text in the textarea"></butt>
        </span>
      </div>
    </div>
    <h4>Preview</h4>
    <pre>{{ text }}</pre>

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

    removeSpace() {
      this.text = this.text.replace(/\s+/g, " ");
    },

    copy() {
      navigator.clipboard.writeText(this.text);
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

p,
pre {
  color: rgba(255, 255, 255, 0.7);
}

h1 {
  text-align: center;
}
</style>
