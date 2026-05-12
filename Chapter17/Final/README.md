# JAVA MINI CITY

## Synopsis
This program allows a user to navigate a car around a city map.

## Motivation
I want to improve my understanding of GIS and autonomous vehicles. This project serves to build my skills in the area of mapmaking and vehicle controls.

## How to Run
This program requires JavaFX to display the map and car. The png files required are in this GitHub repository.

## Code Example
A map was created for this program; I had to run multiple tests to ensure the roads aligned with the grid.
```
private static final int TILE_SIZE = 50; 
    private static final int ROWS = 10;
    private static final int COLS = 10;

    // 0 = Building, 1 = Road
    private final int[][] mapData = {
        {0, 0, 1, 0, 0, 0, 0, 0, 1, 0},
        {0, 0, 1, 0, 0, 0, 0, 0, 1, 0},
        {0, 0, 1, 0, 0, 0, 0, 0, 1, 0},
        {1, 1, 1, 1, 1, 1, 1, 1, 1, 1},
        {0, 0, 0, 0, 0, 0, 0, 0, 1, 0},
        {0, 0, 0, 0, 0, 0, 0, 0, 1, 0},
        {0, 0, 0, 0, 0, 0, 0, 0, 1, 0},
        {0, 0, 0, 0, 0, 0, 0, 0, 1, 0},
        {1, 1, 1, 1, 1, 1, 1, 1, 1, 1},
        {0, 0, 0, 0, 0, 0, 0, 0, 1, 0}
    };

    @Override
    public void start(Stage primaryStage) {
        Pane root = new Pane();

        // Upload the map image and set it as the background
        Image mapImage = new Image("https://raw.githubusercontent.com/EmilyRhos/TESD_1800_Software_Development_Coursework/main/Chapter17/Final/Resources/mapv2.png");
        ImageView mapView = new ImageView(mapImage);
        mapView.setFitWidth(COLS * TILE_SIZE);
        mapView.setFitHeight(ROWS * TILE_SIZE);

        root.getChildren().add(mapView);```
