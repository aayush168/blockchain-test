<template>
  <v-app>
    <v-content>
      <PrimaryToolbar/>
      <NavigationToolbar/>
      <Homepage/>
    </v-content>
  </v-app>
</template>

<script>

import PrimaryToolbar from '@/components/toolbar/PrimaryToolbar';
import NavigationToolbar from '@/components/toolbar/NavigationToolbar'
import Homepage from '@/components/Homepage';

export default {
  name: 'App',
  components: {
    PrimaryToolbar,
    Homepage,
    NavigationToolbar
  },
  data () {
    return {
      //
    }
  }
}
</script>
