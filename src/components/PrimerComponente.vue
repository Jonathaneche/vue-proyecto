<template>
  <div>
    <h1>Mi primer componente</h1>
    <p>{{ names[0] }}</p>
    <p>{{ names[1] }}</p>
    <p>{{ names[2] }}</p>
  </div>

  <div>
    <p>
      <b>{{ mensaje.title }}</b>
    </p>
    <p>{{ mensaje.text }}</p>
  </div>

  <div>
    <p v-for="(names, index) in names" :key="index">{{ names }}</p>
  </div>
</template>

<script>
export default {
  setup() {
    const names = ["Jone", "May", "Nasser"];
    const mensaje = {
      title: "What is Lorem Ipsum?",
      text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
    };

    return {
      names,
      mensaje,
    };
  },
};
</script>

<style></style>
