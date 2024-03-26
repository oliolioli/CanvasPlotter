# CanvasPlotter (work in progress) #
CanvasPlot is a very simple plotter designed for straightforward plotting using HTML Canvas and nothing more. 

This project is currently in progress, aimed at providing developers with a lightweight and dependency-free solution for creating simple charts and graphs (for example for your offline IOT-device). The goal is to offer an intuitive lightweight plotting experience that respects user privacy, works offline, and requires no external dependencies.

Of course, there are the well-known charting libraries such as (Plotly)[https://github.com/plotly/plotly.js], Chart.js and D3.js. But even Plotly requires 3.5 MB and consists of compressed ASCII text with very long lines (58407).

Using such JavaScript libraries on small IOT devices is annoying.


## Features ##

- **Dependency-Free**: CanvasPlot is committed to simplicity. It doesn't rely on external libraries, ensuring a streamlined and efficient plotting experience.

- **Offline Functionality**: Embrace the flexibility of working offline. CanvasPlot enables developers to craft engaging visualizations without the need for a constant internet connection, catering to projects in various environments.

- **Privacy-First**: User privacy is a top priority. CanvasPlot refrains from tracking any user data, providing a secure and anonymous plotting environment for both developers and end-users.


## Example plot ##

![plotter](https://github.com/oliolioli/CanvasPlotter/assets/4264535/85bb7ab8-ddd7-4eae-87b7-21f63dfb4fe2)


## Howto configure your simple canvas plotter ##

### Configure size of plot ###

```
var GRAPH_TOP = 25;
var GRAPH_BOTTOM = 375; 
var GRAPH_LEFT = 35;
var GRAPH_RIGHT = 480;   
var GRAPH_HEIGHT = 350; 
var GRAPH_WIDTH = 450;
```

### Get maximum of measuring points (for each curve) ###

```
// get max temp to draw right y-axis (= temp and also dew point)
var largestTemp = 0;  
for( var i = 0; i < tempGraph.length; i++ ){  
    if( tempGraph[ i ] > largestTemp ){  
        largestTemp = tempGraph[ i ] + 5;  
    }  
}
```

Rename function if needed.


### Drawing graph temperature legend ###

```
context.font = "italic 12px Arial";  
context.fillStyle = "black";
context.fillText( "Temperature", GRAPH_RIGHT, (GRAPH_BOTTOM) + 40);
context.fillStyle = "red";  
context.fillText( "Dew point", GRAPH_RIGHT, (GRAPH_BOTTOM) + 60 );
context.fillStyle = "#002080";  
context.fillText( "Humidity", GRAPH_LEFT - 30, (GRAPH_BOTTOM) + 50 );
```

# Contributions #
This project welcomes contributions and feedback! If you encounter issues, have suggestions, or want to contribute improvements, feel free to open an issue or submit a pull request.
