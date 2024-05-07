<template>
  <div>
    <h1 :class="{ active: isActive }" :style="{ fontSize: fontSize + 'px' }">{{ title }}</h1>
    <input type="text" v-model="inputValue" @input="handleInput" placeholder="Masukkan teks disini...">
    <p>Input value: {{ inputValue }}</p>
    <button @click="increaseFontSize">Besarkan Judul</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hi Kawan Teknikku',
      isActive: false,
      fontSize: 24,
      inputValue: ''
    }
  },
  methods: {
    handleInput() {
      this.isActive = !this.isActive;
    },
    increaseFontSize() {
      this.fontSize += 1;
    },
  
  }
}
</script>

<style>
.active {
  color: red;
}
</style>