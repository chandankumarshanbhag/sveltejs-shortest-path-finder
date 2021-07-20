<script>
    import { range } from "lodash";

    let twoDArray = range(25).map((x) => range(25));
    let obstaclesMap = {};

    function setObstacle(x, y) {
        obstaclesMap[x] = obstaclesMap[x] || {};
        obstaclesMap[x][y] = !obstaclesMap[x][y];
        console.log(obstaclesMap);
    }
</script>

<div class="nes-container with-title is-dark root-playarea">
    <div class="nes-table-responsive">
        <table class="nes-table is-bordered is-dark is-centered">
            <tbody>
                {#each twoDArray as oneDArray, x}
                    <tr>
                        {#each oneDArray as item,y}
                            <td class={obstaclesMap[x] && obstaclesMap[x][y] ? "obstacle":""} on:click={() => setObstacle(x,y)} />
                        {/each}
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
</div>

<style>
    .root-playarea {
        flex: 1;
        margin: 0 0.5rem;
        height: 100%;
    }
    td {
    }
    .obstacle{
        background-color: brown;
    }
</style>
