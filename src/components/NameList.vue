<template>
  <div>
    <h3 v-for="name in names" :key="name.firstName">
      <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
    </h3>
  </div>
</template>

<script>
export default {
  name: "NameList",
  data() {
    return {
      names: [
        {
          firstName: "Bruce",
          lastName: "Wayne",
        },
        {
          firstName: "Tony",
          lastName: "Stark",
        },
        {
          firstName: "Stephen",
          lastName: "Strange",
        },
      ],
    };
  },
};
</script>

<style scoped></style>
