<script setup>
import docx2html from "docx2html";
const handleSubmit = (e) => {
  docx2html(e.target.files[0], {
    container: document.querySelector("#my-file"),
  }).then((html) => {
    //do some change if needed
  });
};
</script>

<template>
  <div>
    <h1>Docx Component</h1>
    <form @submit="handleSubmit">
      <input type="file" @change="handleSubmit" />
    </form>
    <div id="my-file" class="board"></div>
  </div>
</template>
a
<style scoped>
.board {
  border: 1px solid black;
}
</style>
