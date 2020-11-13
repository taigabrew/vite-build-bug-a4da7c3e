<template>
  <button @click="send">Send message to worker</button>
</template>

<script>
import SimpleWorker from './simple.worker.js?worker'

export default {
  name: 'App',
  setup() {
    const worker = new SimpleWorker()

    return {
      send() {
        worker.postMessage('foo')
      },
    }
  },
}
</script>
