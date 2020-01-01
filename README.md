# LucidFrame
LucidFrame Is Framework for Make A Game in Browser,

# If you are very comfortable working and innovating in a web browser, this Framework is perfect for you, Overall Made in Native Javascript, and some Html or css standards.
# This Framework Does Not Use Canvas Today Or SVG As Basic Rendering of Various Objects that you create, But Objects will still look good.
# let's contribute to developing this framework.

# Greetings, Ziddan Strife.
# Thanks.



  let mapOption = {
      size: {
          sizeType: "px",
          xSize: 2000,
          ySize: 800,
          xBlockSize: 50,
          yBlockSize: 50,
          perspective: 1000,
      },
      debugMode: false,
  }
  let blockOption = {
      blockOpacity: 0.8,
      borderSize: 0.2,
      backgroundColor: 'gray',
      blockConfig: []
  }

  // write block config for set different block
  let line1 = [];
  line1.push({
      from: '0.11', to: '39.11', class: "ceramic-white" // format:'x.y' & input the class
      //note: must be 1 straight line
  })
  line1.push({from: '0.12', to: '39.12' , class: "ceramic-white"});
  line1.push({from: '18.13', to: '20.13' , class: "ceramic-white"});
  line1.push({from: '0.14', to: '39.14' , class: "ceramic-white"});
  line1.push({from: '0.15', to: '39.15' , class: "ceramic-white"});
  blockOption.blockConfig.push({
      line: line1, // line must be array
      lineId: "line_one" // optional
  })

  var mapObj = createMap("#mainMap", mapOption, blockOption);
  mapObj.generateMap();
  let cube1 = mapObj.createObject('cube', {size: 50, backgroundColor: 'green', opacity: 1, borderColor: 'yellow'});
  mapObj.putInObject(cube1, {bottom: '-172px', position: {x: 0, y: 0}});

  let cube2 = mapObj.createObject('cube', {size: 100, backgroundColor: 'darkblue', opacity: 1, borderColor: 'blue'});
  mapObj.putInObject(cube2, {bottom: '-172px', position: {x: 0, y: 9}});

  let cube3 = mapObj.createObject('cube', {size: 50, backgroundColor: 'skyblue', opacity: 1, borderColor: 'blue'});
  mapObj.putInObject(cube3, {bottom: '-172px', position: {x: 0, y: 13}});
