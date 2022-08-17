<template>
  <tr class="cursor-pointer hover">
    <td>{{ user.name }}</td>
    <td>{{ user.age }}</td>
    <td>{{ user.class }}</td>
  </tr>
</template>

<script setup lang="ts">
import { User } from "./../stores/user";
defineProps({
  user: { type: User, required: true },
});
</script>

<style scoped></style>
