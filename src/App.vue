<script setup>

import { storeUser } from "./store/user";

const checkLogin = () => {
  return storeUser().getUserId;
}

if(!checkLogin()) {
  window.location.href='#/login';
}

</script>

<template>
  <router-view></router-view>
</template>
