# phaser-cheatsheet

```
let config = {
    type: Phaser.AUTO,
    width: 800,
    height: 600,
    physics: {
        default: 'arcade',
        arcade: {
            gravity: false,
            debug: false
        }
    },
     scene: {
        preload: preload,
        create: create,
        update: update
    }
}
``` 
    
var game = new Phaser.Game(config);

```
function preload(){
    this.load.image('building', 'assets/base1.png');
    this.load.spritesheet('dude', 'assets/dude.png', { frameWidth: 32, frameHeight: 48 });
}
```

let grupa = this.physics.add.group();

grupa.add(x,y,srpite);
player.tint = '0xffff00';
this.physics.world.setBounds(0, 0, 800, 600);

player.setInteractive();

```
    player.on('pointerdown', () => {
        console.log(player.clicked);
       if(!player.clicked){
       player.tint = '0xffff00';
        player.clicked = true;
        }else{
       player.tint = '0xffffff';

            player.clicked = false;
        }

    })
    
    this.input.on('pointerdown', (pointer) => {
    console.log(pointer.x ,pointer.y)
    })
    
   ```
   ```
          this.physics.moveToObject(player, target, 100);
```

PRZYCISKI
```
          cursors = this.input.keyboard.createCursorKeys();
           if (cursors.up.isDown) {
                jump();
            }
            
                var keyboard = this.input.keyboard;
 if (keyboard.addKey('A').isDown) {
                enemy.setVelocityX(-160);
                enemy.anims.play('left', true);
            }

 this.input.keyboard.addListener('keydown_SPACE', function (event) {
      console.log('fsdaddsf');
      shoot(this);
   }, this);

    ```
    
    CZAS
    
    ```
          this.time.addEvent({
                delay: 10000,
                loop: true,
                callback: function () {
                    addDudeEnemy();
                }
            })
            ```
            
            ```
                   this.physics.add.collider(dudesenemy, base1, attackbase, null, this);
                   ```

