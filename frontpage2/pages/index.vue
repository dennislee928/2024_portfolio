<template>
  <NewHeader />
  <!-- First Divider -->
  <div class="divider"></div>
  <div class="title">
    <h1 class="first-title">Dennis Lee</h1>

    <h3 class="second-title">Savior or Manic?</h3>
  </div>
  <!-- Second Divider -->
  <div class="divider"></div>
  <CV />
  <!-- Third Divider -->
  <div class="divider"></div>
  <Works />
</template>

<script setup></script>
<style>
.divider {
  width: 100%;
  height: 2px;
  background-color: black;
  margin-top: 15px; /* Adjust spacing as needed */
}
.title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  font-family: "Old Newspaper Types", serif;
  margin: 5px;
}
.first-title {
  font-size: 100px;
}
.second-title {
  font-size: 60px;
}
</style>
