<template>
  <div class="container">
    <div class="character">
      <div class="name">{{ name }}</div>
      <div class="image"><img v-bind:src="image" /></div>
      <div class="list">
        <ul>
          <li>Status: {{ status }}</li>
          <li>Species {{ species }}</li>
          <li>Type: {{ type }}</li>
          <li>Gender: {{ gender }}</li>
          <li>Created: {{ created }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: [
    "id",
    "name",
    "image",
    "status",
    "species",
    "type",
    "gender",
    "created",
    "next",
    "prev",
  ],
};
</script>

<style>
.character {
  background-color: #ccc;
  font-size: 15px;
  box-shadow: 1px 1px 7px -3px rgba(66, 68, 90, 1);
  border-radius: 5px;
  display: flex;
  flex-wrap: wrap;
  width: 220px;
  height: 420px;
  padding: 10px;
  transition: background-color 400ms;
  opacity: 0.9;
}
.character:hover {
  background-color: #fff;
}

ul {
  list-style-type: none;
  display: flex;
  display: block;
  margin-left: 0;
  margin-right: auto;
  margin:auto;
  
  
}
.name {
  text-align: center;
  font-size: 150%;
}

img {
  width: 80%;
  height: auto;
  margin-bottom: 10px;
}
.image {
  display: flex;
  align-items: center;
  justify-content: center;
}

div {
  margin: 10px;
  line-height: 1.3;
}
</style>
