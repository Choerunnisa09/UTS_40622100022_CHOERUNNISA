<template>
  <div class="text-display">Hai Kamu berumur {{ count }} yaa?</div><br>
  <button @click="increment">Tambah</button>
</template>
<script>
  export default {
    // Properties returned from data() become reactive state
    // and will be exposed on `this`.
    data() {
      return {
        count: 0
      }
    },
  
    // Methods are functions that mutate state and trigger updates.
    // They can be bound as event handlers in templates.
    methods: {
      increment() {
        this.count++
      }
    },
  
    // Lifecycle hooks are called at different stages
    // of a component's lifecycle.
    // This function will be called when the component is mounted.
    mounted() {
      console.log(`The initial count is ${this.count}.`)
    }
  }
  </script>

<style scoped>
  .container {
    text-align: center;
    margin-top: 70px;
  }
  
  .text-display {
    margin-bottom: 20px;
  }
  </style>