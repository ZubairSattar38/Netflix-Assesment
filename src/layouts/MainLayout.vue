<template>
  <q-layout view="lHh Lpr lFf">
     <q-drawer
      v-model="rightDrawerOpen"
      bordered
        side="right"
      content-class="bg-grey-1"
    >
        <q-scroll-area style="height: calc(100% - 150px); margin-top: 150px; border-right: 1px solid #ddd">
          <q-list padding>
            <q-item clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="inbox" />
              </q-item-section>
              <q-item-section>
                Inbox
        <q-tooltip content-class="bg-purple" content-style="font-size: 16px" :offset="[10, 10]">
                     Inbox Tooltip
                </q-tooltip>
              </q-item-section>
            </q-item>
            <q-item active clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="star" />
              </q-item-section>
              <q-item-section>
                Star
        <q-tooltip content-class="bg-amber" content-style="font-size: 16px" :offset="[10, 10]">
                     Star Tooltip
                </q-tooltip>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="send" />
              </q-item-section>

              <q-item-section>
                Send
        <q-tooltip content-class="bg-red" content-style="font-size: 16px" :offset="[10, 10]">
                     Send Tooltip
                </q-tooltip>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="drafts" />
              </q-item-section>

              <q-item-section>
                Drafts
        <q-tooltip content-class="bg-indigo" content-style="font-size: 16px" :offset="[10, 10]">
                     Drafts Tooltip
                </q-tooltip>
              </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>
        <q-img class="absolute-top" src="https://cdn.quasar.dev/img/material.png" style="height: 150px">
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="56px" class="q-mb-sm">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar>
            <div class="text-weight-bold">Zubair Sattar</div>
            <div>Self Made</div>
          </div>
        </q-img>
    </q-drawer>
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
            <q-img src="../statics/logo/netflixlogo.png" style="width:170px"></q-img>
        </q-toolbar-title>

        <div class="gt-sm">
        </div>
        <div>
            <q-btn
              flat
              dense
              round
              @click="rightDrawerOpen =! rightDrawerOpen"
              icon="menu"
              aria-label="Menu"
            />
        </div>

      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',
  data () {
    return {
      rightDrawerOpen: false
    }
  }
}
</script>
