<template>
  <div class="password-generator">
    <button class="generate-btn" @click="generatePassword">
      Generate Password
    </button>
    <p v-if="password">{{ password }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: '',
    };
  },
  methods: {
    generatePassword() {
      const length = 10;
      const charset = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
      let retVal = '';
      for (let i = 0, n = charset.length; i < length; ++i) {
        retVal += charset.charAt(Math.floor(Math.random() * n));
      }
      this.password = retVal;
    },
  },
};
</script>

<style scoped>
.password-generator {
  font-size: 12px;
  text-align: center;
}

.generate-btn {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  transition-duration: 0.4s;
  border-radius: 10px; /* Add this line */
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2); /* Add this line */
}

.generate-btn:hover {
  background-color: #45a049;
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2); /* Add this line */
}
</style>