<template>
  <div class="container">
      <div class="main-row">
        <div id="twitch-embed" class="tile">
        </div>
        <div id="twitch-embed-t" class="tile">
        </div>
      </div>

      <div class="sub-row">
        <div id="twitch-embed-3" class="tile">
        </div>
        <div class="tile">
        </div>
        <div class="tile">
        </div>
        <div class="tile">
        </div>
        <div class="tile">
        </div>
                <div class="tile">
        </div>

      </div>
  </div>
</template>

<script>

    export default {
        name: 'MultiStream',
        props: {
            msg: String
        },
        mounted() {
            let options = {
                width: '100%',
                height: '100%',
                channel: "Nickmercs",
                layout: "video"
            };
            new window.Twitch.Embed("twitch-embed", options);
            // var player = new window.Twitch.Player("<player div ID>", options);
            // console.log(player)

            let options2 = {
                width: '100%',
                height: '100%',
                channel: "xqcow",
                layout: "video"
            };
            new window.Twitch.Embed("twitch-embed-t", options2);
            // let player2 = new window.Twitch.Player("twitch-embed-t", options2);
            // console.log(player2)
                        let options3 = {
                width: '100%',
                height: '100%',
                channel: "imaqtpie",
                layout: "video"
            };
            new window.Twitch.Embed("twitch-embed-3", options3);
        }
    }
    
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
    display: flex;
    flex-direction: column;
    height: 100%;
}

.main-row {
    display: flex;
    flex-grow: 1;
    flex-direction: row;
    height: 500px;
}

.sub-row {
    display: flex;
    flex-grow: 1;
    height: 200px;
    margin-top: 10px;
}

.tile {
    flex-grow: 1;
    background-color: aqua;
    margin: 0px 5px;
}

.aqua-div {
    flex-grow: 2;
    background-color: aqua;
}

.brown-div {
    flex-grow: 1;
    background-color:brown;
}
</style>
