<script setup>
defineProps({
  itemName: {
    type: String,
    required: true
  },
  itemLink: {
    type: String,
    required: true
  }
})
</script>

<template>
    <li>
        <a href="{{ itemLink }}">{{ itemName }}</a>
    </li>
</template>

<style scoped>

li{
  list-style: none;
  width: fit-content;
}

a{
  color: #FFF;
  text-align: right;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  width: 100%;
  height: 100%;
}

li:hover a{
  background-color: transparent;
  color: #b81366;
}

</style>