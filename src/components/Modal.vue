<template>
  <div class="modal">
    <div class="modal-content">
      <header>
        <slot name="header">
          <h2>Default header</h2>
        </slot>
        <button @click="$emit('close')">X</button>
      </header>
      <section>
        <slot name="content">
          <p>Default content</p>
        </slot>
      </section>
      <footer>
        <slot name="footer">
          <button @click="$emit('close')">Close</button>
        </slot>
      </footer>
    </div>
  </div>
</template>

<script setup>
import {defineProps} from 'vue'

defineProps({
  show: Boolean
})
</script>

<style scoped>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  color: var(--text);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  width: 900px;
  max-height: 80vh;
  overflow-y: auto;
  color: var(--text);
  background-color: #333;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);


  scrollbar-width: thin;
  scrollbar-color: var(--primary) var(--secondary);
  scrollbar-track-color: #333;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #000000;
  padding-bottom: 10px;
}

footer {
  display: flex;
  justify-content: flex-end;
  margin-top: 10px;
}

header button {
  background-color: #ce0f0f;
  border: 1px solid #ce0f0f;
  color: #ffffff;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1rem;
}

header button:hover {
  background-color: #b20c0c;
  border: 1px solid #b20c0c;
  opacity: 0.8;
}

footer button {
  background-color: var(--primary);
  color: #ffffff;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 100px;
  font-size: 1rem;
}

footer button:hover {
  background-color: var(--secondary);
  opacity: 0.8;
}
</style>