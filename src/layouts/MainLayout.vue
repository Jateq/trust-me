<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-tabs class="nav-bar" v-model="tab">
        <q-tab name="logo" label="logo" />
        <q-tab name="TrustPlaces" label="TrustPlaces" />
        <q-tab name="TrustPeople" label="TrustPeople" />
        <q-tab name="TrustCompany" label="TrustCompany" />
        <q-tab name="TrustCoin" label="TrustCoin" />
        <q-tab name="TrustBusiness" label="TrustBusiness" />
        <q-tab name="TrustContract" label="TrustContract" />
        <q-tab name="More" label="More" />
        <q-tab name="number" label="+77000700455" />
        <q-tab name="Ru" label="Ru" />
      </q-tabs>
    </q-header>


    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

export default {
  name: 'MainLayout',
  components: {
  },
  data() {
    return {
      tab: "TrustPlaces"
    };
  }
}
</script>
