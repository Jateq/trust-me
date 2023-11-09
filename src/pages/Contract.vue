<template>
  <q-page >
    <div class="left-nav-tool">

            <div>
              <div class="drawer-container" :class="{'mini-state': miniState} ">
                <div class="drawer-content">
                  <div class="drawer-item">
                    <div class="avatar">
                      <q-icon name="house" />
                    </div>
                    <div class="section">
                      Компания
                    </div>
                  </div>

                  <div class="drawer-item">
                    <div class="avatar">
                      <q-icon name="history_edu" />
                    </div>
                    <div class="section">
                      Шаблоны
                    </div>
                  </div>

                  <div class="drawer-item">
                    <div class="avatar">
                      <q-icon name="edit_note" />
                    </div>
                    <div class="section">
                      Мои контракты
                    </div>
                  </div>

                  <div class="drawer-item">
                    <div class="avatar">
                      <q-icon name="auto_stories" />
                    </div>
                    <div class="section">
                      Архив
                    </div>
                  </div>

                  <div class="drawer-item">
                    <div class="avatar">
                      <q-icon name="account_circle" />
                    </div>
                    <div class="section">
                      Аккаунт
                    </div>
                  </div>

                </div>
              </div>
            </div>

        </div>

    <div class="main-contract">
        <button class="show-paper" @click="showA4Page">
          <span>Посмотреть договор</span>
          <q-icon class="main-contract-expand" :name="expandIcon"></q-icon>
        </button>
        <div  v-if="showPaper">
          <A4Page/>
        </div>
    </div>

    <div class="right-logic">

    </div>
  </q-page>
</template>

<script>

import A4Page from 'components/ContractPaper.vue'
export default {
  components: {
    A4Page
  },
  data() {
    return {
      miniState: false,
      showPaper: false,
      isExpanded: false
    };
    name: 'PageIndex'
  },
  methods: {
    showA4Page() {
      this.showPaper = !this.showPaper;
      this.isExpanded = !this.isExpanded;
    },
  },
  computed: {
    expandIcon() {
      return this.isExpanded ? 'expand_less' : 'expand_more';
    }
  }
};
</script>
