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

          <A4Page/>

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

    };
    name: 'PageIndex'
  },
  methods: {

  },
  computed: {

  }
};
</script>
