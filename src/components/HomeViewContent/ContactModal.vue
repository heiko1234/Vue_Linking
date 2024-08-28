<template>
  <div class="modalrapper" v-if="isModalVisible">
    <div class="backdrop" @click="closeModal">
      <div class="modal">
        <header>
          <h1>Contacts</h1>
        </header>
        <section>
          <p class="content">
            {{ contacts }}
          </p>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactModal',
  props: {
    contacts: {
      type: String,
      required: false
    },
    isModalVisible: {
      type: Boolean,
      required: true
    }
  },
  methods: {
    closeModal() {
      this.$emit('closeModal')
      console.log('toggleModal closeModal: ', this.isModalVisible)
    }
  }
}
</script>

<style scoped>
.backdrop {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
}

.modal {
  width: 90%;
  max-width: 40rem;
  background: white;
  border-radius: 6px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  z-index: 10;
  overflow: hidden;
}
</style>
