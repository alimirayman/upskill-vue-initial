<template>
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" >
    {{ jobTitle }}
    @
    <a :href="companyURL" target="_blank">{{ companyName }}</a>
  </div>
</template>

<script>
export default {
  props: {
    jobTitle: String,
    companyURL: String,
    companyName: String,
  }
}
</script>