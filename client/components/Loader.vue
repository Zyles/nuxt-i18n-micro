<template>
  <div class="loader-container">
    <div class="loader">
      <div class="loader-circle" />
      <div class="loader-text">
        Loading...
      </div>
    </div>
  </div>
</template>

<style scoped>
.loader-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100px;
  padding: 20px;
}

.loader {
  text-align: center;
}

.loader-circle {
  display: inline-block;
  width: 40px;
  height: 40px;
  border: 4px solid #f3f3f3;
  border-radius: 50%;
  border-top: 4px solid #3498db;
  animation: spin 1s linear infinite;
  margin-bottom: 8px;
}

.loader-text {
  color: #666;
  font-size: 14px;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
</style>
