<template>
  <div>

    {{ msg }}
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
// import Rx from 'rxjs/Rx'

// import Rx from 'rxjs'

// Rx.Observable.of(1,2,3)

import { Observable} from 'rxjs/Observable';
import 'rxjs/add/observable/of';
import 'rxjs/add/operator/map';

const msg = Observable.of(1,2,3).map(x => x + '!!!').subscribe(n => console.log(n));

export default Vue.extend({
  created() {
  }
})
</script>
<style scoped>

</style>
