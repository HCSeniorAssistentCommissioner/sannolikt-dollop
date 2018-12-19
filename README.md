< script  src = " ../ src / lib / pixi.min.js " > </ script >
< script  src = " " ../src/main.js " " > </ script >
var renderer = PIXI.autoDetectRenderer(window.innerWidth, window.innerHeight);
function init()
{
    renderer.backgroundColor = 0x22A7F0;
    renderer.render(stage);
    loop();
}
class CloudManager
{
    constructor()
    {
    }
    update()
    {
    }
}
<script src="../src/lib/pixi.min.js"></script>
<script src="../src/CloudManager.js"></script>
<script src="../src/main.js"></script>
window.setInterval(function()
{
}
, 1000);
PIXI.loader.add([
    "assets/cloud_1.png",
    "assets/cloud_2.png"
]).load(init);
window.setInterval(function()
{
    const sprite = (Math.random() > 0.5 ? "cloud_1" : "cloud_2");
    this.cloud = new PIXI.Sprite(PIXI.loader.resources["assets/" + sprite + ".png"].texture);
    this.cloud.anchor.set(0.5, 0.5);
    this.cloud.position.set(renderer.width * 1.2, renderer.height * Math.random());
    stage.addChild(this.cloud);
}
, 1000);
this.cloudsList = [];
this.cloudsList.push(this.cloud);
this.cloudsList.forEach(function(element) {
    element.position.x -= 4;
});
