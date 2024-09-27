# Chess-App

<a target="_blank" href="https://sumit-chessapp.netlify.app/" target="_blank">Chess App</a>
### The HTML creates the chessboard with 8x8 squares using div elements, each assigned a unique ID based on coordinates. 
1. Global Styles:
Reset margin and padding for all elements and set box-sizing to border-box.
Set html and body to full width and height, and hide overflow.

2. Body Styles:
Apply a gradient background from purple to blue.
Set text color to white.

3. Root Variables:
Define CSS custom properties (variables) for colors.

4. Turn Display:
Style the turn display with padding, border, and background color changes.
5. Game Board:
Define styles for the game board container (#game), setting maximum dimensions and centering it.
Style cell prefixes and game cells with borders, dimensions, and hover effects.

6. Game Cells:
Apply transitions, border-radius, and hover effects with animations for game cells.
Define background colors for alternating cell colors (grey and green).

7. Text Animations:
Create neon glow effects using keyframe animations for different text colors (blue, orange, green).

8. Shake Animations:
Define a shake-little animation to create a shaking effect with various keyframe steps.


## HTML Code
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Basic Chess App</title>
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <div id="game">
      <div class="cellprefix">8</div>
      <div class="gamecell" id="1_8"></div>
      <div class="gamecell grey" id="2_8"></div>
      <div class="gamecell" id="3_8"></div>
      <div class="gamecell grey" id="4_8"></div>
      <div class="gamecell" id="5_8"></div>
      <div class="gamecell grey" id="6_8"></div>
      <div class="gamecell" id="7_8"></div>
      <div class="gamecell grey" id="8_8"></div>

      <div class="cellprefix">7</div>
      <div class="gamecell grey" id="1_7"></div>
      <div class="gamecell" id="2_7"></div>
      <div class="gamecell grey" id="3_7"></div>
      <div class="gamecell" id="4_7"></div>
      <div class="gamecell grey" id="5_7"></div>
      <div class="gamecell" id="6_7"></div>
      <div class="gamecell grey" id="7_7"></div>
      <div class="gamecell" id="8_7"></div>

      <div class="cellprefix">6</div>
      <div class="gamecell" id="1_6"></div>
      <div class="gamecell grey" id="2_6"></div>
      <div class="gamecell" id="3_6"></div>
      <div class="gamecell grey" id="4_6"></div>
      <div class="gamecell" id="5_6"></div>
      <div class="gamecell grey" id="6_6"></div>
      <div class="gamecell" id="7_6"></div>
      <div class="gamecell grey" id="8_6"></div>

      <div class="cellprefix">5</div>
      <div class="gamecell grey" id="1_5"></div>
      <div class="gamecell" id="2_5"></div>
      <div class="gamecell grey" id="3_5"></div>
      <div class="gamecell" id="4_5"></div>
      <div class="gamecell grey" id="5_5"></div>
      <div class="gamecell" id="6_5"></div>
      <div class="gamecell grey" id="7_5"></div>
      <div class="gamecell" id="8_5"></div>

      <div class="cellprefix">4</div>
      <div class="gamecell" id="1_4"></div>
      <div class="gamecell grey" id="2_4"></div>
      <div class="gamecell" id="3_4"></div>
      <div class="gamecell grey" id="4_4"></div>
      <div class="gamecell" id="5_4"></div>
      <div class="gamecell grey" id="6_4"></div>
      <div class="gamecell" id="7_4"></div>
      <div class="gamecell grey" id="8_4"></div>

      <div class="cellprefix">3</div>
      <div class="gamecell grey" id="1_3"></div>
      <div class="gamecell" id="2_3"></div>
      <div class="gamecell grey" id="3_3"></div>
      <div class="gamecell" id="4_3"></div>
      <div class="gamecell grey" id="5_3"></div>
      <div class="gamecell" id="6_3"></div>
      <div class="gamecell grey" id="7_3"></div>
      <div class="gamecell" id="8_3"></div>

      <div class="cellprefix">2</div>
      <div class="gamecell" id="1_2"></div>
      <div class="gamecell grey" id="2_2"></div>
      <div class="gamecell" id="3_2"></div>
      <div class="gamecell grey" id="4_2"></div>
      <div class="gamecell" id="5_2"></div>
      <div class="gamecell grey" id="6_2"></div>
      <div class="gamecell" id="7_2"></div>
      <div class="gamecell grey" id="8_2"></div>

      <div class="cellprefix">1</div>
      <div class="gamecell grey" id="1_1"></div>
      <div class="gamecell" id="2_1"></div>
      <div class="gamecell grey" id="3_1"></div>
      <div class="gamecell" id="4_1"></div>
      <div class="gamecell grey" id="5_1"></div>
      <div class="gamecell" id="6_1"></div>
      <div class="gamecell grey" id="7_1"></div>
      <div class="gamecell" id="8_1"></div>

      <div class="cellprefix"></div>
      <div class="cellprefix">a</div>
      <div class="cellprefix">b</div>
      <div class="cellprefix">c</div>
      <div class="cellprefix">d</div>
      <div class="cellprefix">e</div>
      <div class="cellprefix">f</div>
      <div class="cellprefix">g</div>
      <div class="cellprefix">h</div>

      <div class="turn" id="turn">Its White turn</div>
    </div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>

    <script src="script.js"></script>
  </body>
</html>

```

### StyleSheet
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html,
body {
    width: 100%;
    height: 100%;
    font-family: sans-serif;
    overflow: hidden;
}



body {
    background: linear-gradient(purple, blue);
    color: #fff;
}

:root {
    --green: #5cb85c;
    --glassgreen: #00a4a2;
}


.turn {
    color: black;
    padding: 10px;
    right: -55px;

}

#turn {
    max-width: 451px;
    max-height: 30px;
    width: 100%;
    height: 100%;
    position: relative;
    float: left;
    border-right: 5px;
    border: 1px solid rgba(0, 0, 0);
    border-style: inset;
    text-align: center;
    background: #fff;
    transition: .85s linear;
}

.turnheightlight {
    background: var(--green) !important;
    color: #fff;
}

#game {
    max-width: 504px;
    max-height: 504px;
    width: 100%;
    height: 100%;
    position: relative;
    margin: 20px auto;
}

.cellprefix {
    width: 100%;
    height: 100%;
    max-height: 50px;
    max-width: 50px;
    float: left;
    margin: 3px;
    padding: 15px 0 0 20px;
}

.gamecell {
    border: 1px solid var(--glassgreen);
    width: 100%;
    height: 100%;
    max-height: 50px;
    max-width: 50px;
    float: left;
    margin: 3px;
    transition: all 0.5s ease-in-out;
    border-radius: 5px;
    padding: 0 0 0 6px;
    font-size: 30pt;
    cursor: pointer;
    z-index: 1;
}

.gamecell:hover {
    color: #fff;
    background: rgba(37, 88, 228, 0.7);
    z-index: 2;
    transform: translate(10px, -10px);
    animation: neonBlueText 1.5s ease-in-out infinite alternate;
}

.grey {
    background: rgba(43, 42, 42, 0.8);
}

.green {
    background: rgb(65, 161, 73) !important;
}

.neonorange_txt {
    animation: neonOrangeText 1.5s ease-in-out infinite alternate;
}

neongreen_txt {
    animation: neonGreenText 1.5s ease-in-out infinite alternate;
}

@keyframes neonBlueText {
    from {
        text-shadow: 0 0 10px #fff,
            0 0 20px #fff,
            0 0 30px #fff,
            0 0 40px #228dff,
            0 0 70px #228dff,
            0 0 80px #228dff,
            0 0 100px #228dff,
            0 0 150px #228dff;
    }

    to {
        text-shadow: 0 0 5px #fff,
            0 0 10px #fff,
            0 0 15px #fff,
            0 0 20px #228dff,
            0 0 35px #228dff,
            0 0 40px #228dff,
            0 0 50px #228dff,
            0 0 75px #228dff;
    }
}

@keyframes neonIrangeText {
    from {
        text-shadow: 0 0 10px #fff,
            0 0 20px #fff,
            0 0 30px #fff,
            0 0 40px #f90,
            0 0 70px #f90,
            0 0 80px #f90,
            0 0 100px #f90,
            0 0 150px #f90;
    }

    to {
        text-shadow: 0 0 5px #fff,
            0 0 10px #fff,
            0 0 15px #fff,
            0 0 20px #f90,
            0 0 35px #f90,
            0 0 40px #f90,
            0 0 50px #f90,
            0 0 75px #f90;
    }
}

@keyframes neonGreenText {
    from {
        text-shadow: 0 0 10px #fff,
            0 0 20px #fff,
            0 0 30px #fff,
            0 0 40px #b6ff00,
            0 0 70px #b6ff00,
            0 0 80px #b6ff00,
            0 0 100px #b6ff00,
            0 0 150px #b6ff00;
    }

    to {
        text-shadow: 0 0 5px #fff,
            0 0 10px #fff,
            0 0 15px #fff,
            0 0 20px #b6ff00,
            0 0 35px #b6ff00,
            0 0 40px #b6ff00,
            0 0 50px #b6ff00,
            0 0 75px #b6ff00;
    }
}

/* let me add some css classes to move your DOM */

.shake-little {
    display: inline-block;
    transform-origin: center center;
}

.shake-freeze,
.shake-constant,
.shake-constent--hover:hover,
.shake-trigger:hover,
.shake-constant-hover {
    animation-play-state: running;
}

.shake-freeze:hover,
.shake-trigger:hover,
.shake-freeze,
.shake-little:hover,
.shake-trigger:hover,
.shake-little {
    animation-play-state: running;
}

@keyframes shake-little {
    2% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    4% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    6% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    8% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    10% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    12% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    14% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    16% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    18% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    20% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    22% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    24% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    26% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    28% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    30% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    32% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    34% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    36% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    38% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    40% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    42% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    44% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    46% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    48% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    50% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    52% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    54% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    56% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    58% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    60% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    62% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    64% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    66% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    68% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    70% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    72% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    74% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    76% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    78% {
        transform: translate(0px, 0px) rotate(0.5deg);
    }

    80% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    82% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    84% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    86% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    88% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    90% {
        transform: translate(0px, 1px) rotate(0.5deg);
    }

    92% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    94% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    96% {
        transform: translate(1px, 0px) rotate(0.5deg);
    }

    98% {
        transform: translate(1px, 1px) rotate(0.5deg);
    }

    0%,
    100% {
        transform: translate(0, 0) rotate(0);
    }
}
```

### Javacscript Code
```
let main = {
  variables: {
    turn: "w",
    selectedpiece: "",
    highlighted: [],
    pieces: {
      w_king: {
        position: "5_1",
        img: "&#9812;",
        captured: false,
        moved: false,
        type: "w_king",
      },
      w_queen: {
        position: "4_1",
        img: "&#9813;",
        captured: false,
        moved: false,
        type: "w_queen",
      },
      w_bishop1: {
        position: "3_1",
        img: "&#9815;",
        captured: false,
        moved: false,
        type: "w_bishop",
      },
      w_bishop2: {
        position: "6_1",
        img: "&#9815;",
        captured: false,
        moved: false,
        type: "w_bishop",
      },
      w_knight1: {
        position: "2_1",
        img: "&#9816;",
        captured: false,
        moved: false,
        type: "w_knight",
      },
      w_knight2: {
        position: "7_1",
        img: "&#9816;",
        captured: false,
        moved: false,
        type: "w_knight",
      },
      w_rook1: {
        position: "1_1",
        img: "&#9814;",
        captured: false,
        moved: false,
        type: "w_rook",
      },
      w_rook2: {
        position: "8_1",
        img: "&#9814;",
        captured: false,
        moved: false,
        type: "w_rook",
      },
      w_pawn1: {
        position: "1_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn2: {
        position: "2_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn3: {
        position: "3_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn4: {
        position: "4_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn5: {
        position: "5_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn6: {
        position: "6_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn7: {
        position: "7_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },
      w_pawn8: {
        position: "8_2",
        img: "&#9817;",
        captured: false,
        type: "w_pawn",
        moved: false,
      },

      b_king: {
        position: "5_8",
        img: "&#9818;",
        captured: false,
        moved: false,
        type: "b_king",
      },
      b_queen: {
        position: "4_8",
        img: "&#9819;",
        captured: false,
        moved: false,
        type: "b_queen",
      },
      b_bishop1: {
        position: "3_8",
        img: "&#9821;",
        captured: false,
        moved: false,
        type: "b_bishop",
      },
      b_bishop2: {
        position: "6_8",
        img: "&#9821;",
        captured: false,
        moved: false,
        type: "b_bishop",
      },
      b_knight1: {
        position: "2_8",
        img: "&#9822;",
        captured: false,
        moved: false,
        type: "b_knight",
      },
      b_knight2: {
        position: "7_8",
        img: "&#9822;",
        captured: false,
        moved: false,
        type: "b_knight",
      },
      b_rook1: {
        position: "1_8",
        img: "&#9820;",
        captured: false,
        moved: false,
        type: "b_rook",
      },
      b_rook2: {
        position: "8_8",
        img: "&#9820;",
        captured: false,
        moved: false,
        type: "b_rook",
      },
      b_pawn1: {
        position: "1_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn2: {
        position: "2_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn3: {
        position: "3_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn4: {
        position: "4_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn5: {
        position: "5_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn6: {
        position: "6_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn7: {
        position: "7_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
      b_pawn8: {
        position: "8_7",
        img: "&#9823;",
        captured: false,
        type: "b_pawn",
        moved: false,
      },
    },
  },

  methods: {
    gamesetup: function () {
      $(".gamecell").attr("chess", "null");
      for (let gamepiece in main.variables.pieces) {
        $("#" + main.variables.pieces[gamepiece].position).html(
          main.variables.pieces[gamepiece].img
        );
        $("#" + main.variables.pieces[gamepiece].position).attr(
          "chess",
          gamepiece
        );
      }
    },

    moveoptions: function (selectedpiece) {
      let position = { x: "", y: "" };
      position.x = main.variables.pieces[selectedpiece].position.split("_")[0];
      position.y = main.variables.pieces[selectedpiece].position.split("_")[1];

      // these options need to be var instead of let
      var options = [];
      var coordinates = [];
      var startpoint = main.variables.pieces[selectedpiece].position;
      var c1, c2, c3, c4, c5, c6, c7, c8;

      if (main.variables.highlighted.length != 0) {
        main.methods.togglehighlight(main.variables.highlighted);
      }

      switch (main.variables.pieces[selectedpiece].type) {
        case "w_king":
          if (
            $("#6_1").attr("chess") == "null" &&
            $("#7_1").attr("chess") == "null" &&
            main.variables.pieces["w_king"].moved == false &&
            main.variables.pieces["w_rook2"].moved == false
          ) {
            coordinates = [
              { x: 1, y: 1 },
              { x: 1, y: 0 },
              { x: 1, y: -1 },
              { x: 0, y: -1 },
              { x: -1, y: -1 },
              { x: -1, y: 0 },
              { x: -1, y: 1 },
              { x: 0, y: 1 },
              { x: 2, y: 0 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          } else {
            coordinates = [
              { x: 1, y: 1 },
              { x: 1, y: 0 },
              { x: 1, y: -1 },
              { x: 0, y: -1 },
              { x: -1, y: -1 },
              { x: -1, y: 0 },
              { x: -1, y: 1 },
              { x: 0, y: 1 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          }

          options = main.methods
            .options(
              startpoint,
              coordinates,
              main.variables.pieces[selectedpiece].type
            )
            .slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "b_king":
          if (
            $("#6_8").attr("chess") == "null" &&
            $("#7_8").attr("chess") == "null" &&
            main.variables.pieces["b_king"].moved == false &&
            main.variables.pieces["b_rook2"].moved == false
          ) {
            coordinates = [
              { x: 1, y: 1 },
              { x: 1, y: 0 },
              { x: 1, y: -1 },
              { x: 0, y: -1 },
              { x: -1, y: -1 },
              { x: -1, y: 0 },
              { x: -1, y: 1 },
              { x: 0, y: 1 },
              { x: 2, y: 0 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          } else {
            coordinates = [
              { x: 1, y: 1 },
              { x: 1, y: 0 },
              { x: 1, y: -1 },
              { x: 0, y: -1 },
              { x: -1, y: -1 },
              { x: -1, y: 0 },
              { x: -1, y: 1 },
              { x: 0, y: 1 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          }
          /*
                      coordinates = [{ x: 1, y: 1 },{ x: 1, y: 0 },{ x: 1, y: -1 },{ x: 0, y: -1 },{ x: -1, y: -1 },{ x: -1, y: 0 },{ x: -1, y: 1 },{ x: 0, y: 1 }].map(function(val){
                        return (parseInt(position.x) + parseInt(val.x)) + '_' + (parseInt(position.y) + parseInt(val.y));
                      });
                    */
          options = main.methods
            .options(
              startpoint,
              coordinates,
              main.variables.pieces[selectedpiece].type
            )
            .slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "w_queen":
          c1 = main.methods.w_options(position, [
            { x: 1, y: 1 },
            { x: 2, y: 2 },
            { x: 3, y: 3 },
            { x: 4, y: 4 },
            { x: 5, y: 5 },
            { x: 6, y: 6 },
            { x: 7, y: 7 },
          ]);
          c2 = main.methods.w_options(position, [
            { x: 1, y: -1 },
            { x: 2, y: -2 },
            { x: 3, y: -3 },
            { x: 4, y: -4 },
            { x: 5, y: -5 },
            { x: 6, y: -6 },
            { x: 7, y: -7 },
          ]);
          c3 = main.methods.w_options(position, [
            { x: -1, y: 1 },
            { x: -2, y: 2 },
            { x: -3, y: 3 },
            { x: -4, y: 4 },
            { x: -5, y: 5 },
            { x: -6, y: 6 },
            { x: -7, y: 7 },
          ]);
          c4 = main.methods.w_options(position, [
            { x: -1, y: -1 },
            { x: -2, y: -2 },
            { x: -3, y: -3 },
            { x: -4, y: -4 },
            { x: -5, y: -5 },
            { x: -6, y: -6 },
            { x: -7, y: -7 },
          ]);
          c5 = main.methods.w_options(position, [
            { x: 1, y: 0 },
            { x: 2, y: 0 },
            { x: 3, y: 0 },
            { x: 4, y: 0 },
            { x: 5, y: 0 },
            { x: 6, y: 0 },
            { x: 7, y: 0 },
          ]);
          c6 = main.methods.w_options(position, [
            { x: 0, y: 1 },
            { x: 0, y: 2 },
            { x: 0, y: 3 },
            { x: 0, y: 4 },
            { x: 0, y: 5 },
            { x: 0, y: 6 },
            { x: 0, y: 7 },
          ]);
          c7 = main.methods.w_options(position, [
            { x: -1, y: 0 },
            { x: -2, y: 0 },
            { x: -3, y: 0 },
            { x: -4, y: 0 },
            { x: -5, y: 0 },
            { x: -6, y: 0 },
            { x: -7, y: 0 },
          ]);
          c8 = main.methods.w_options(position, [
            { x: 0, y: -1 },
            { x: 0, y: -2 },
            { x: 0, y: -3 },
            { x: 0, y: -4 },
            { x: 0, y: -5 },
            { x: 0, y: -6 },
            { x: 0, y: -7 },
          ]);

          coordinates = c1
            .concat(c2)
            .concat(c3)
            .concat(c4)
            .concat(c5)
            .concat(c6)
            .concat(c7)
            .concat(c8);

          options = coordinates.slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "b_queen":
          c1 = main.methods.b_options(position, [
            { x: 1, y: 1 },
            { x: 2, y: 2 },
            { x: 3, y: 3 },
            { x: 4, y: 4 },
            { x: 5, y: 5 },
            { x: 6, y: 6 },
            { x: 7, y: 7 },
          ]);
          c2 = main.methods.b_options(position, [
            { x: 1, y: -1 },
            { x: 2, y: -2 },
            { x: 3, y: -3 },
            { x: 4, y: -4 },
            { x: 5, y: -5 },
            { x: 6, y: -6 },
            { x: 7, y: -7 },
          ]);
          c3 = main.methods.b_options(position, [
            { x: -1, y: 1 },
            { x: -2, y: 2 },
            { x: -3, y: 3 },
            { x: -4, y: 4 },
            { x: -5, y: 5 },
            { x: -6, y: 6 },
            { x: -7, y: 7 },
          ]);
          c4 = main.methods.b_options(position, [
            { x: -1, y: -1 },
            { x: -2, y: -2 },
            { x: -3, y: -3 },
            { x: -4, y: -4 },
            { x: -5, y: -5 },
            { x: -6, y: -6 },
            { x: -7, y: -7 },
          ]);
          c5 = main.methods.b_options(position, [
            { x: 1, y: 0 },
            { x: 2, y: 0 },
            { x: 3, y: 0 },
            { x: 4, y: 0 },
            { x: 5, y: 0 },
            { x: 6, y: 0 },
            { x: 7, y: 0 },
          ]);
          c6 = main.methods.b_options(position, [
            { x: 0, y: 1 },
            { x: 0, y: 2 },
            { x: 0, y: 3 },
            { x: 0, y: 4 },
            { x: 0, y: 5 },
            { x: 0, y: 6 },
            { x: 0, y: 7 },
          ]);
          c7 = main.methods.b_options(position, [
            { x: -1, y: 0 },
            { x: -2, y: 0 },
            { x: -3, y: 0 },
            { x: -4, y: 0 },
            { x: -5, y: 0 },
            { x: -6, y: 0 },
            { x: -7, y: 0 },
          ]);
          c8 = main.methods.b_options(position, [
            { x: 0, y: -1 },
            { x: 0, y: -2 },
            { x: 0, y: -3 },
            { x: 0, y: -4 },
            { x: 0, y: -5 },
            { x: 0, y: -6 },
            { x: 0, y: -7 },
          ]);

          coordinates = c1
            .concat(c2)
            .concat(c3)
            .concat(c4)
            .concat(c5)
            .concat(c6)
            .concat(c7)
            .concat(c8);

          options = coordinates.slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;

        case "w_bishop":
          c1 = main.methods.w_options(position, [
            { x: 1, y: 1 },
            { x: 2, y: 2 },
            { x: 3, y: 3 },
            { x: 4, y: 4 },
            { x: 5, y: 5 },
            { x: 6, y: 6 },
            { x: 7, y: 7 },
          ]);
          c2 = main.methods.w_options(position, [
            { x: 1, y: -1 },
            { x: 2, y: -2 },
            { x: 3, y: -3 },
            { x: 4, y: -4 },
            { x: 5, y: -5 },
            { x: 6, y: -6 },
            { x: 7, y: -7 },
          ]);
          c3 = main.methods.w_options(position, [
            { x: -1, y: 1 },
            { x: -2, y: 2 },
            { x: -3, y: 3 },
            { x: -4, y: 4 },
            { x: -5, y: 5 },
            { x: -6, y: 6 },
            { x: -7, y: 7 },
          ]);
          c4 = main.methods.w_options(position, [
            { x: -1, y: -1 },
            { x: -2, y: -2 },
            { x: -3, y: -3 },
            { x: -4, y: -4 },
            { x: -5, y: -5 },
            { x: -6, y: -6 },
            { x: -7, y: -7 },
          ]);

          coordinates = c1.concat(c2).concat(c3).concat(c4);

          options = coordinates.slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;

        case "b_bishop":
          c1 = main.methods.b_options(position, [
            { x: 1, y: 1 },
            { x: 2, y: 2 },
            { x: 3, y: 3 },
            { x: 4, y: 4 },
            { x: 5, y: 5 },
            { x: 6, y: 6 },
            { x: 7, y: 7 },
          ]);
          c2 = main.methods.b_options(position, [
            { x: 1, y: -1 },
            { x: 2, y: -2 },
            { x: 3, y: -3 },
            { x: 4, y: -4 },
            { x: 5, y: -5 },
            { x: 6, y: -6 },
            { x: 7, y: -7 },
          ]);
          c3 = main.methods.b_options(position, [
            { x: -1, y: 1 },
            { x: -2, y: 2 },
            { x: -3, y: 3 },
            { x: -4, y: 4 },
            { x: -5, y: 5 },
            { x: -6, y: 6 },
            { x: -7, y: 7 },
          ]);
          c4 = main.methods.b_options(position, [
            { x: -1, y: -1 },
            { x: -2, y: -2 },
            { x: -3, y: -3 },
            { x: -4, y: -4 },
            { x: -5, y: -5 },
            { x: -6, y: -6 },
            { x: -7, y: -7 },
          ]);

          coordinates = c1.concat(c2).concat(c3).concat(c4);

          options = coordinates.slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);
          break;
        case "w_knight":
          coordinates = [
            { x: -1, y: 2 },
            { x: 1, y: 2 },
            { x: 1, y: -2 },
            { x: -1, y: -2 },
            { x: 2, y: 1 },
            { x: 2, y: -1 },
            { x: -2, y: -1 },
            { x: -2, y: 1 },
          ].map(function (val) {
            return (
              parseInt(position.x) +
              parseInt(val.x) +
              "_" +
              (parseInt(position.y) + parseInt(val.y))
            );
          });

          options = main.methods
            .options(
              startpoint,
              coordinates,
              main.variables.pieces[selectedpiece].type
            )
            .slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "b_knight":
          coordinates = [
            { x: -1, y: 2 },
            { x: 1, y: 2 },
            { x: 1, y: -2 },
            { x: -1, y: -2 },
            { x: 2, y: 1 },
            { x: 2, y: -1 },
            { x: -2, y: -1 },
            { x: -2, y: 1 },
          ].map(function (val) {
            return (
              parseInt(position.x) +
              parseInt(val.x) +
              "_" +
              (parseInt(position.y) + parseInt(val.y))
            );
          });

          options = main.methods
            .options(
              startpoint,
              coordinates,
              main.variables.pieces[selectedpiece].type
            )
            .slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "w_rook":
          c1 = main.methods.w_options(position, [
            { x: 1, y: 0 },
            { x: 2, y: 0 },
            { x: 3, y: 0 },
            { x: 4, y: 0 },
            { x: 5, y: 0 },
            { x: 6, y: 0 },
            { x: 7, y: 0 },
          ]);
          c2 = main.methods.w_options(position, [
            { x: 0, y: 1 },
            { x: 0, y: 2 },
            { x: 0, y: 3 },
            { x: 0, y: 4 },
            { x: 0, y: 5 },
            { x: 0, y: 6 },
            { x: 0, y: 7 },
          ]);
          c3 = main.methods.w_options(position, [
            { x: -1, y: 0 },
            { x: -2, y: 0 },
            { x: -3, y: 0 },
            { x: -4, y: 0 },
            { x: -5, y: 0 },
            { x: -6, y: 0 },
            { x: -7, y: 0 },
          ]);
          c4 = main.methods.w_options(position, [
            { x: 0, y: -1 },
            { x: 0, y: -2 },
            { x: 0, y: -3 },
            { x: 0, y: -4 },
            { x: 0, y: -5 },
            { x: 0, y: -6 },
            { x: 0, y: -7 },
          ]);

          coordinates = c1.concat(c2).concat(c3).concat(c4);

          options = coordinates.slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "b_rook":
          c1 = main.methods.b_options(position, [
            { x: 1, y: 0 },
            { x: 2, y: 0 },
            { x: 3, y: 0 },
            { x: 4, y: 0 },
            { x: 5, y: 0 },
            { x: 6, y: 0 },
            { x: 7, y: 0 },
          ]);
          c2 = main.methods.b_options(position, [
            { x: 0, y: 1 },
            { x: 0, y: 2 },
            { x: 0, y: 3 },
            { x: 0, y: 4 },
            { x: 0, y: 5 },
            { x: 0, y: 6 },
            { x: 0, y: 7 },
          ]);
          c3 = main.methods.b_options(position, [
            { x: -1, y: 0 },
            { x: -2, y: 0 },
            { x: -3, y: 0 },
            { x: -4, y: 0 },
            { x: -5, y: 0 },
            { x: -6, y: 0 },
            { x: -7, y: 0 },
          ]);
          c4 = main.methods.b_options(position, [
            { x: 0, y: -1 },
            { x: 0, y: -2 },
            { x: 0, y: -3 },
            { x: 0, y: -4 },
            { x: 0, y: -5 },
            { x: 0, y: -6 },
            { x: 0, y: -7 },
          ]);

          coordinates = c1.concat(c2).concat(c3).concat(c4);

          options = coordinates.slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
        case "w_pawn":
          if (main.variables.pieces[selectedpiece].moved == false) {
            coordinates = [
              { x: 0, y: 1 },
              { x: 0, y: 2 },
              { x: 1, y: 1 },
              { x: -1, y: 1 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          } else if (main.variables.pieces[selectedpiece].moved == true) {
            coordinates = [
              { x: 0, y: 1 },
              { x: 1, y: 1 },
              { x: -1, y: 1 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          }

          options = main.methods
            .options(
              startpoint,
              coordinates,
              main.variables.pieces[selectedpiece].type
            )
            .slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;

        case "b_pawn":
          // calculate pawn options
          if (main.variables.pieces[selectedpiece].moved == false) {
            coordinates = [
              { x: 0, y: -1 },
              { x: 0, y: -2 },
              { x: 1, y: -1 },
              { x: -1, y: -1 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          } else if (main.variables.pieces[selectedpiece].moved == true) {
            coordinates = [
              { x: 0, y: -1 },
              { x: 1, y: -1 },
              { x: -1, y: -1 },
            ].map(function (val) {
              return (
                parseInt(position.x) +
                parseInt(val.x) +
                "_" +
                (parseInt(position.y) + parseInt(val.y))
              );
            });
          }

          options = main.methods
            .options(
              startpoint,
              coordinates,
              main.variables.pieces[selectedpiece].type
            )
            .slice(0);
          main.variables.highlighted = options.slice(0);
          main.methods.togglehighlight(options);

          break;
      }
    },

    options: function (startpoint, coordinates, piecetype) {
      // first check if any of the possible coordinates is out of bounds;

      coordinates = coordinates.filter((val) => {
        let pos = { x: 0, y: 0 };
        pos.x = parseInt(val.split("_")[0]);
        pos.y = parseInt(val.split("_")[1]);

        if (!(pos.x < 1) && !(pos.x > 8) && !(pos.y < 1) && !(pos.y > 8)) {
          // if it is not out of bounds, return the coordinate;
          return val;
        }
      });

      switch (piecetype) {
        case "w_king":
          coordinates = coordinates.filter((val) => {
            return (
              $("#" + val).attr("chess") == "null" ||
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "b"
            );
          });

          break;
        case "b_king":
          coordinates = coordinates.filter((val) => {
            return (
              $("#" + val).attr("chess") == "null" ||
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "w"
            );
          });

          break;
        case "w_knight":
          coordinates = coordinates.filter((val) => {
            return (
              $("#" + val).attr("chess") == "null" ||
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "b"
            );
          });

          break;

        case "b_knight":
          coordinates = coordinates.filter((val) => {
            return (
              $("#" + val).attr("chess") == "null" ||
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "w"
            );
          });

          break;

        case "w_pawn":
          coordinates = coordinates.filter((val) => {
            let sp = { x: 0, y: 0 };
            let coordinate = val.split("_");

            sp.x = startpoint.split("_")[0];
            sp.y = startpoint.split("_")[1];

            if (coordinate[0] < sp.x || coordinate[0] > sp.x) {
              // if the coordinate is on either side of the center, check if it has an opponent piece on it;
              return (
                $("#" + val).attr("chess") != "null" &&
                $("#" + val)
                  .attr("chess")
                  .slice(0, 1) == "b"
              ); // return coordinates with opponent pieces on them
            } else {
              // else if the coordinate is in the center;
              if (
                coordinate[1] == parseInt(sp.y) + 2 &&
                $("#" + sp.x + "_" + (parseInt(sp.y) + 1)).attr("chess") !=
                  "null"
              ) {
                // do nothing if this is the pawns first move, and there is a piece in front of the 2nd coordinate;
              } else {
                return $("#" + val).attr("chess") == "null"; // otherwise return the coordinate if there is no chess piece on it;
              }
            }
          });

          break;

        case "b_pawn":
          coordinates = coordinates.filter((val) => {
            let sp = { x: 0, y: 0 };
            let coordinate = val.split("_");

            sp.x = startpoint.split("_")[0];
            sp.y = startpoint.split("_")[1];

            if (coordinate[0] < sp.x || coordinate[0] > sp.x) {
              // if the coordinate is on either side of the center, check if it has an opponent piece on it;
              return (
                $("#" + val).attr("chess") != "null" &&
                $("#" + val)
                  .attr("chess")
                  .slice(0, 1) == "w"
              ); // return coordinates with opponent pieces on them
            } else {
              // else if the coordinate is in the center;
              if (
                coordinate[1] == parseInt(sp.y) - 2 &&
                $("#" + sp.x + "_" + (parseInt(sp.y) - 1)).attr("chess") !=
                  "null"
              ) {
                // do nothing if this is the pawns first move, and there is a piece in front of the 2nd coordinate;
              } else {
                return $("#" + val).attr("chess") == "null"; // otherwise return the coordinate if there is no chess piece on it;
              }
            }
          });

          break;
      }

      return coordinates;
    },

    w_options: function (position, coordinates) {
      let flag = false;

      coordinates = coordinates
        .map(function (val) {
          // convert the x,y into actual grid id coordinates;
          return (
            parseInt(position.x) +
            parseInt(val.x) +
            "_" +
            (parseInt(position.y) + parseInt(val.y))
          );
        })
        .filter((val) => {
          let pos = { x: 0, y: 0 };
          pos.x = parseInt(val.split("_")[0]);
          pos.y = parseInt(val.split("_")[1]);

          if (!(pos.x < 1) && !(pos.x > 8) && !(pos.y < 1) && !(pos.y > 8)) {
            // if it is not out of bounds, return the coordinate;
            return val;
          }
        })
        .filter((val) => {
          // algorithm to determine line-of-sight movement options for bishop/rook/queen;
          if (flag == false) {
            if ($("#" + val).attr("chess") == "null") {
              console.log(val);
              return val;
            } else if (
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "b"
            ) {
              flag = true;
              console.log(val);
              return val;
            } else if (
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "w"
            ) {
              console.log(val + "-3");
              flag = true;
            }
          }
        });

      return coordinates;
    },

    b_options: function (position, coordinates) {
      let flag = false;

      coordinates = coordinates
        .map(function (val) {
          // convert the x,y into actual grid id coordinates;
          return (
            parseInt(position.x) +
            parseInt(val.x) +
            "_" +
            (parseInt(position.y) + parseInt(val.y))
          );
        })
        .filter((val) => {
          let pos = { x: 0, y: 0 };
          pos.x = parseInt(val.split("_")[0]);
          pos.y = parseInt(val.split("_")[1]);

          if (!(pos.x < 1) && !(pos.x > 8) && !(pos.y < 1) && !(pos.y > 8)) {
            // if it is not out of bounds, return the coordinate;
            return val;
          }
        })
        .filter((val) => {
          // algorithm to determine line-of-sight movement options for bishop/rook/queen;
          if (flag == false) {
            if ($("#" + val).attr("chess") == "null") {
              return val;
            } else if (
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "w"
            ) {
              flag = true;
              return val;
            } else if (
              $("#" + val)
                .attr("chess")
                .slice(0, 1) == "b"
            ) {
              flag = true;
            }
          }
        });

      return coordinates;
    },

    capture: function (target) {
      let selectedpiece = {
        name: $("#" + main.variables.selectedpiece).attr("chess"),
        id: main.variables.selectedpiece,
      };

      //new cell
      $("#" + target.id).html(main.variables.pieces[selectedpiece.name].img);
      $("#" + target.id).attr("chess", selectedpiece.name);
      //old cell
      $("#" + selectedpiece.id).html("");
      $("#" + selectedpiece.id).attr("chess", "null");
      //moved piece
      main.variables.pieces[selectedpiece.name].position = target.id;
      main.variables.pieces[selectedpiece.name].moved = true;
      // captured piece
      main.variables.pieces[target.name].captured = true;
      /*
            // toggle highlighted coordinates
            main.methods.togglehighlight(main.variables.highlighted);
            main.variables.highlighted.length = 0;
            // set the selected piece to '' again
            main.variables.selectedpiece = '';
            */
    },

    move: function (target) {
      let selectedpiece = $("#" + main.variables.selectedpiece).attr("chess");

      // new cell
      $("#" + target.id).html(main.variables.pieces[selectedpiece].img);
      $("#" + target.id).attr("chess", selectedpiece);
      // old cell
      $("#" + main.variables.selectedpiece).html("");
      $("#" + main.variables.selectedpiece).attr("chess", "null");
      main.variables.pieces[selectedpiece].position = target.id;
      main.variables.pieces[selectedpiece].moved = true;

      /*
            // toggle highlighted coordinates
            main.methods.togglehighlight(main.variables.highlighted);
            main.variables.highlighted.length = 0;
            // set the selected piece to '' again
            main.variables.selectedpiece = '';
            */
    },

    endturn: function () {
      if (main.variables.turn == "w") {
        main.variables.turn = "b";

        // toggle highlighted coordinates
        main.methods.togglehighlight(main.variables.highlighted);
        main.variables.highlighted.length = 0;
        // set the selected piece to '' again
        main.variables.selectedpiece = "";

        $("#turn").html("It's Blacks Turn");

        $("#turn").addClass("turnhighlight");
        window.setTimeout(function () {
          $("#turn").removeClass("turnhighlight");
        }, 1500);
      } else if ((main.variables.turn = "b")) {
        main.variables.turn = "w";

        // toggle highlighted coordinates
        main.methods.togglehighlight(main.variables.highlighted);
        main.variables.highlighted.length = 0;
        // set the selected piece to '' again
        main.variables.selectedpiece = "";

        $("#turn").html("It's Whites Turn");

        $("#turn").addClass("turnhighlight");
        window.setTimeout(function () {
          $("#turn").removeClass("turnhighlight");
        }, 1500);
      }
    },

    togglehighlight: function (options) {
      options.forEach(function (element, index, array) {
        $("#" + element).toggleClass("green shake-little neongreen_txt");
      });
    },
  },
};

$(document).ready(function () {
  main.methods.gamesetup();

  $(".gamecell").click(function (e) {
    var selectedpiece = {
      name: "",
      id: main.variables.selectedpiece,
    };

    if (main.variables.selectedpiece == "") {
      selectedpiece.name = $("#" + e.target.id).attr("chess");
    } else {
      selectedpiece.name = $("#" + main.variables.selectedpiece).attr("chess");
    }

    var target = {
      name: $(this).attr("chess"),
      id: e.target.id,
    };

    if (
      main.variables.selectedpiece == "" &&
      target.name.slice(0, 1) == main.variables.turn
    ) {
      // show options

      // moveoptions
      main.variables.selectedpiece = e.target.id;
      main.methods.moveoptions($(this).attr("chess"));
    } else if (main.variables.selectedpiece != "" && target.name == "null") {
      // move selected piece piece

      if (selectedpiece.name == "w_king" || selectedpiece.name == "b_king") {
        let t0 = (selectedpiece.name = "w_king");
        let t1 = (selectedpiece.name = "b_king");
        let t2 = main.variables.pieces[selectedpiece.name].moved == false;
        let t3 = main.variables.pieces["b_rook2"].moved == false;
        let t4 = main.variables.pieces["w_rook2"].moved == false;
        let t5 = target.id == "7_8";
        let t6 = target.id == "7_1";

        if (t0 && t2 && t4 && t6) {
          // castle w_king

          let k_position = "5_1";
          let k_target = "7_1";
          let r_position = "8_1";
          let r_target = "6_1";

          main.variables.pieces["w_king"].position = "7_1";
          main.variables.pieces["w_king"].moved = true;
          $("#" + k_position).html("");
          $("#" + k_position).attr("chess", "null");
          $("#" + k_target).html(main.variables.pieces["w_king"].img);
          $("#" + k_target).attr("chess", "w_king");

          main.variables.pieces["w_rook2"].position = "6_1";
          main.variables.pieces["w_rook2"].moved = true;
          $("#" + r_position).html("");
          $("#" + r_position).attr("chess", "null");
          $("#" + r_target).html(main.variables.pieces["w_rook2"].img);
          $("#" + r_target).attr("chess", "w_rook2");

          main.methods.endturn();
        } else if (t1 && t2 && t3 && t5) {
          // castle b_king

          let k_position = "5_8";
          let k_target = "7_8";
          let r_position = "8_8";
          let r_target = "6_8";

          // w_king
          main.variables.pieces["b_king"].position = "7_8";
          main.variables.pieces["b_king"].moved = true;
          $("#" + k_position).html("");
          $("#" + k_position).attr("chess", "null");
          $("#" + k_target).html(main.variables.pieces["b_king"].img);
          $("#" + k_target).attr("chess", "b_king");

          main.variables.pieces["b_rook2"].position = "6_8";
          main.variables.pieces["b_rook2"].moved = true;
          $("#" + r_position).html("");
          $("#" + r_position).attr("chess", "null");
          $("#" + r_target).html(main.variables.pieces["b_rook2"].img);
          $("#" + r_target).attr("chess", "b_rook2");

          main.methods.endturn();
        } else {
          // move selectedpiece
          main.methods.move(target);
          main.methods.endturn();
        }
      } else {
        // else if selecedpiece.name is not white/black king than move

        main.methods.move(target);
        main.methods.endturn();
      }
    } else if (
      main.variables.selectedpiece != "" &&
      target.name != "null" &&
      target.id != selectedpiece.id &&
      selectedpiece.name.slice(0, 1) != target.name.slice(0, 1)
    ) {
      // capture a piece

      if (
        selectedpiece.id != target.id &&
        main.variables.highlighted.indexOf(target.id) != -1
      ) {
        // if it's not trying to capture pieces not in its movement range

        // capture
        main.methods.capture(target);
        main.methods.endturn();
      }
    } else if (
      main.variables.selectedpiece != "" &&
      target.name != "null" &&
      target.id != selectedpiece.id &&
      selectedpiece.name.slice(0, 1) == target.name.slice(0, 1)
    ) {
      // toggle move options

      // toggle
      main.methods.togglehighlight(main.variables.highlighted);
      main.variables.highlighted.length = 0;

      main.variables.selectedpiece = target.id;
      main.methods.moveoptions(target.name);
    }
  });

  $("body").contextmenu(function (e) {
    e.preventDefault();
  });
});

```
