<script>
import {games} from './data-games.js'
import {onMount} from 'svelte'

onMount( async() => {
    const url = 'http://localhost/back/get-games.php'
    let res = await fetch(url)
    res = await res.json()
    let data = await res.data
    $games = res.data
    console.log(res.data)
})
</script>

<div class="flex-container">
    {#each $games as game (game.id)}
        <div class="cover {game.cover_dimensions}">
            <a href={game.link}><img src={game.cover_image} alt=""></a>
        </div>
    {/each}
</div>

<style>

.flex-container {
    display: flex;
    margin: 0 auto;
    flex-flow: wrap;
    max-width: 1000px;
    justify-content: flex-start;
}

.flex-container img {
    width: 100%;
    padding: 5px;
    border-radius: 10px;
    box-sizing: border-box;
}

.flex-container img:hover {
    background-color: rgba(43, 162, 199, 0.664);
    cursor: pointer;
}

.flex-container .cover {
    display: flex;
    align-items: center;
}

.flex-container .nes {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .ps2 {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .xbox {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .gcn {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .xbox360 {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .wii {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .xboxone {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .segams {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .segagenesis {
    flex: 4 4 125px;
    max-width: 250px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .snes {
    flex: 8 8 250px;
    max-width: 500px;
    min-height: 125px;
    max-height: auto;
}

.flex-container .n64 {
    flex: 8 8 250px;
    max-width: 500px;
    min-height: 125px;
    max-height: auto;
}

.flex-container .steam {
    flex: 8 8 250px;
    max-width: 500px;
    min-height: 125px;
    max-height: auto;
}

.flex-container .psx {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .download {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .gb {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .gbc {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .gba {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .ds {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .n3ds {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .newn3ds {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .segadreamcast {
    flex: 6 6 166.666666px;
    max-width: 333.333333px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .ps3 {
    flex: 5 5 142.857142857px;
    max-width: 285.714285714px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .ps4 {
    flex: 5 5 142.857142857px;
    max-width: 285.714285714px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .psv {
    flex: 5 5 142.857142857px;
    max-width: 285.714285714px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .switch {
    flex: 5 5 133.333333333px;
    max-width: 266.666666667px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .psp {
    flex: 5 5 133.333333333px;
    max-width: 266.666666667px;
    max-height: auto;
    box-sizing: border-box;
}

.flex-container .segasaturn {
    flex: 5 5 133.333333333px;
    max-width: 266.666666667px;
    max-height: auto;
    box-sizing: border-box;
}

</style>