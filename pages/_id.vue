<template>
  <section class="container">
    <h1>Origin: {{ origin }}</h1>
    <br />
    <pre>
    {{params}}
    {{$route.params}}
    "{{typeof $route.params.id}}" should be equal to "{{typeof params.id}}"
    </pre>
  </section>
</template>

<script>
export default {
  asyncData({ params }) {
    return {
      origin: process.server ? "server" : "client",
      params
    };
  }
};
</script>
