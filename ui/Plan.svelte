<style>
.demo-widget {
  background: #f1f1f1;
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 70%;
  cursor: grab;
}

.demo-container {
  max-width: 900px;;
  width: 100%;
  
}

.resizer {
  position: absolute;
  bottom: 3px;
  right: 3px;
  cursor: move;
}
</style>


<div class=demo-container>

<Grid gap={[5, 5]} bind:items={items} rowHeight={50} let:item let:dataItem cols={cols} fastStart={true}>
  <div class="demo-widget">
    {@html dataItem.id}
    
  </div>
</Grid>
</div>

<script>
let filter = {
	"date":'2021-09-06'
}
export let apikey;
export let apiurl;

import Grid from "svelte-grid";
import gridHelp from "svelte-grid/build/helper/index.mjs";

const GRID_WIDTH = 32

let items = [
  { [GRID_WIDTH]: gridHelp.item({ x: 0, 	y: 0, w: 4, h: 1,  fixed: true}),  id: 'ЛИНИЯ:' },
  { [GRID_WIDTH]: gridHelp.item({ x: 4, 	y: 0, w: 4, h: 1,  fixed: true}),  id: '11. OKT' },
  { [GRID_WIDTH]: gridHelp.item({ x: 8, 	y: 0, w: 4, h: 1,  fixed: true}),  id: '12. OKT' },
  { [GRID_WIDTH]: gridHelp.item({ x: 12, 	y: 0, w: 4, h: 1,  fixed: true}),  id: '13. OKT' },
  { [GRID_WIDTH]: gridHelp.item({ x: 16, 	y: 0, w: 4, h: 1, fixed: true }), id: '14. OKT' },
  { [GRID_WIDTH]: gridHelp.item({ x: 20, 	y: 0, w: 4, h: 1, fixed: true }), id: '15. OKT' },
  { [GRID_WIDTH]: gridHelp.item({ x: 24, 	y: 0, w: 4, h: 1, fixed: true }), id: '16. OKT' },
  { [GRID_WIDTH]: gridHelp.item({ x: 28, 	y: 0, w: 4, h: 1, fixed: true }), id: '17. OKT' },
  
  { [GRID_WIDTH]: gridHelp.item({ x: 0,	y: 1, w: 4, h: 4,  fixed: true}),  id: 'РЕЗКА<br/>ПОЛУ-АВТО' },
  { [GRID_WIDTH]: gridHelp.item({ x: 0,	y: 5, w: 4, h: 4,  fixed: true}),  id: 'РЕЗКА<br/>АВТО' },
  
  { [GRID_WIDTH]: gridHelp.item({ x: 4,	y: 1, w: 4, h: 2 }),  id: 'EPS 100<br/>1000x1200<br/>100<br/>30m3' },
  { [GRID_WIDTH]: gridHelp.item({ x: 4,	y: 3, w: 4, h: 2 }),  id: 'EPS 60' },
  { [GRID_WIDTH]: gridHelp.item({ x: 4,	y: 5, w: 4, h: 2 }),  id: 'EPS 200<br/>1000x1200<br/>100<br/>30m3' },
];

const cols = [[ 960, GRID_WIDTH ]];

</script>

