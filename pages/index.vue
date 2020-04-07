<template>
  <v-card>
    <v-card-text>
      <div class="title">Sparkline bug (may be in other components)</div>

      <v-sparkline
        :value="[1,2,3,4,3,2,2,1,4,5,8,6,4,7,6,4,1]"
        color="blue"
      />

      Open first in browser (or press F5) - then blue line disappear due to different _uid's.

      However when edit code with HMR blue line turns visible again.

      It cause by different "_uid" in svg[stroke] and linearGradient[id] inside V-Sparkline component.

      Affects only in "Universal" mode.

    </v-card-text>
  </v-card>
</template>

<script>
export default {

}
</script>
