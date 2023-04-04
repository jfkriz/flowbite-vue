<template>
  <div class="vp-raw flex">
    <Avatar v-if="!imageError" status="online" img="https://flowbite.com/docs/images/people/profile-picture-not-found.jpg" @error:img="imageErrorHandler" />
    <Avatar v-else status="online" rounded />
</div>
</template>
<script setup>
import { Avatar } from '../../../../src/index'
import { ref } from 'vue'

let imageError = ref(false)

function imageErrorHandler() {
    imageError.value = true
}
</script>