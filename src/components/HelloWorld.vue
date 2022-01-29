<template>
  <h2 class="text-2xl">Hello World!</h2>
  <p>{{ saudacao }}</p>
</template>

<script>
export default {
  name: 'HelloWorld',
  setup() {
    const saudacao = 'Bom dia!'
    return { saudacao }
  }
}
</script>

<style></style>
