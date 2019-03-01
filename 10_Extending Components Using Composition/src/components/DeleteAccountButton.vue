<template>
  <button type="button" 
    @click="confirmDeleteModalOpen = true"
  >
  <slot></slot>
    <portal to="modals">
      <confirm-delete-modal
        :show="confirmDeleteModalOpen"
        @close="confirmDeleteModalOpen = false"
        :account-id="accountId"
      />
    </portal>
  </button>
</template>

<script>
import ConfirmDeleteModal from "./ConfirmDeleteModal.vue"

export default {
  components: {
    ConfirmDeleteModal
  },
  props: ["accountId"],
  data() {
    return {
      confirmDeleteModalOpen: false
    }
  }
}
</script>
