<template>
<div class="page tab">
  <div class="bd">
    <cells-title>Tab</cells-title>
    <cells type="access">
      <link-cell router-link="/navbar">
        <span slot="body">navbar</span>
      </link-cell>
      <link-cell router-link="/tabbar">
        <span slot="body">tabbar</span>
      </link-cell>
    </cells>
  </div>
</div>
</template>

<script>
import {CellsTitle, Cells, LinkCell} from 'v-weui';

export default {
  components: {
    CellsTitle,
    Cells,
    LinkCell
  }
}
</script>
