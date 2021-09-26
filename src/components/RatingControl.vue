<template>
  <ul>
    <li :class="{ active: activeOption === 'poor' }">
      <button type="button" @click="activate('poor')">poor</button>
    </li>
    <li :class="{ active: activeOption === 'Average' }">
      <button type="button" @click="activate('Average')">Average</button>
    </li>
    <li :class="{ active: activeOption === 'Great' }">
      <button type="button" @click="activate('Great')">Great</button>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      activeOption: null
    };
  },
  methods: {
    activate(option) {
      this.activeOption = option;
    }
  }
};
</script>
<style scoped>
.active {
  border-color: purple;
}
.active button {
  color: #a00078;
}
ul {
  list-style: none;
  margin: 0.5rem 0;
  padding: 0;
  display: flex;
}
li {
  margin: 0;
  border: 1px solid #ccc;
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
button {
  font: inherit;
  border: none;
  border-color: transparent;
  cursor: pointer;
}
</style>
