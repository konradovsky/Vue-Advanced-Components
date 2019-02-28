<template>
  <div>
    <div class="min-h-screen bg-grey-darker p-8">
      <div class="max-w-sm mx-auto">
        <user-settings-form :account-id="accountId"></user-settings-form>
      </div>
    </div>

    <portal to="modals" v-if="showAnnouncement">
      <announcement-modal
        :show="showAnnouncement"
        @close="showAnnouncement = false"
      ></announcement-modal>
    </portal>

    <portal-target name="modals"></portal-target>
  </div>
</template>

<script>
import UserSettingsForm from './components/UserSettingsForm.vue'
import AnnouncementModal from './components/AnnouncementModal.vue'

export default {
  components: {
    UserSettingsForm,
    AnnouncementModal 
  },
  data() {
    return {
      accountId: 3,
      showAnnouncement: true
    }
  }
}
</script>

<style src="./assets/app.css"/>
