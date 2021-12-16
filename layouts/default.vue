<template>
  <v-app dark>
    
    <v-app-bar
      :clipped-left="true"
      :bottom="bottom"
      fixed
      app
    >
    
  
      <v-icon class="pe-5" color="red">mdi-play-box</v-icon>
      <v-toolbar-title v-text="title" ></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-text-field class="ms-5 mt-8 px-3 py-3"
            label="Search..."
            outlined
      ></v-text-field>
         <v-btn><v-icon class="px-1" color="red">mdi-magnify</v-icon></v-btn>
         <v-btn><v-icon class="px-2" color="red">mdi-microphone</v-icon></v-btn>
      <v-spacer></v-spacer>
      <v-spacer />

      <v-btn
              icon
            >
              <v-icon color="red">mdi-apps</v-icon>
      </v-btn>
      <v-btn
              icon
            >
              <v-icon color="red">mdi-dots-vertical</v-icon>
      </v-btn>



      <v-btn
        outlined
        color="red"
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon>mdi-account</v-icon>
        SIGN IN
      </v-btn>
    </v-app-bar>

<v-navigation-drawer
      v-model="drawer"
      :clipped="true"
      fixed
      app
      permanent
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
        
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    
          
          
      
        <v-spacer></v-spacer>
    
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
    </v-navigation-drawer>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-compass',
          title: 'Explore',
          to: '/inspire'
        },
        {
          icon: 'mdi-youtube-subscription',
          title: 'Subscriptions',
          to: '/subscribed'
        },
        {
          icon: '',
          title: '',
          to: '/history'
        },
        {
          icon: 'mdi-play-box-multiple',
          title: 'Library',
          to: '/history'
        },
        {
          icon: 'mdi-history',
          title: 'History',
          to: '/history'
        },
        {
          icon: 'mdi-music',
          title: 'Music',
          to: '/music'
        },
         {
          icon: 'mdi-trophy',
          title: 'Sports',
          to: '/sport'
        },
        {
          icon: 'mdi-youtube-gaming',
          title: 'Gaming',
          to: '/gaming'
        },
        {
          icon: 'mdi-newspaper',
          title: 'News',
          to: '/news'
        },
        {
          icon: 'mdi-access-point',
          title: 'Live',
          to: '/live'
        },
         {
          icon: 'mdi-panorama-sphere-outline',
          title: '360° Video',
          to: '/360video'
        },
        {
          icon: '',
          title: '',
          to: '/360video'
        },
        {
          icon: 'mdi-plus-circle',
          title: 'Browse channels',
          to: '/browsechannels'
        },
        {
          icon: 'mdi-youtube',
          title: 'Youtube Premium',
          to: '/youtubepremium'
        },
        {
          icon: 'mdi-cog-outline',
          title: 'Settings',
          to: '/settings'
        },
        {
          icon: 'mdi-flag-variant-outline',
          title: 'Report history',
          to: '/report'
        },
        {
          icon: 'mdi-help-circle-outline',
          title: 'Help',
          to: '/help'
        },
        {
          icon: 'mdi-message-alert-outline',
          title: 'Send feedback',
          to: '/Send feedback'
        },
      
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Youtube'
    }
  }
}
</script>
