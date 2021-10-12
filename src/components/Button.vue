<template>
  <div>
    <button class="btn">{{ buttonName }}</button>
  </div>
</template>

<script>
export default {
  props: ["buttonName"],
};
</script>

<style>
.btn {
  height: 37px;
  padding: 0 20px;
  border-radius: 6px;
  background-color: #91d8f6;
  font-weight: 700;
  cursor: pointer;
}
</style>
