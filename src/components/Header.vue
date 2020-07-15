<template>
  <div class="row justify-content-center bottom-two">
    <div class="col-6 col-md-8 col-sm-12">
      <h2>Willkommen auf der Webseite von</h2>
      <h1><em>{{ author.name }}</em></h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
#unicorn {
  width: 150px;
  height: auto;
}
</style>
