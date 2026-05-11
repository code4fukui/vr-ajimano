# vr-ajimano

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A VR and 3D map experience showcasing the cherry blossoms of Ajimano Elementary School, created using photogrammetry.

## Demos

- **[3D Model on Map](https://code4fukui.github.io/vr-ajimano/map.html)**: An interactive map displaying the school's 3D model in its geographical location.
- **[VR Ground View](https://code4fukui.github.io/vr-ajimano/ground.html)**: An immersive, ground-level VR tour of the cherry blossoms.
- **[Six Cherry Blossoms in VR](https://code4fukui.github.io/vr-ajimano/sakuras.html)**: A virtual space featuring six cherry blossom tree models arranged in a circle.

## About the Project

This project digitally preserves and shares the scenery of the Ajimano Elementary School's cherry blossoms. It combines photogrammetry-scanned 3D models with WebVR (A-Frame) and 3D mapping (MapLibre GL JS) to create accessible and immersive experiences directly in the browser.

## Features

- **3D Map Integration**: Uses MapLibre GL JS and a custom layer (`getModelLayer.js`) to render a `.glb` model onto a 3D map.
- **Immersive VR Scenes**: Built with A-Frame, featuring teleportation and first-person camera controls (`mc-controls.js`).
- **Photogrammetry Models**: Includes two detailed GLB models: `ajimano-sakura-ground.glb` (tree with surrounding ground) and `ajimano-sakura.glb` (a single tree).
- **Cross-Platform**: Runs on desktop browsers and is compatible with VR headsets that support WebXR.

## Getting Started

To run this project locally, you will need a local web server.

1.  Clone the repository:
    ```sh
    git clone https://github.com/code4fukui/vr-ajimano.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd vr-ajimano
    ```
3.  Start a local web server. For example, using Python:
    ```sh
    python -m http.server
    ```
4.  Open your web browser and navigate to one of the HTML files (e.g., `http://localhost:8000/map.html`).

## Key Components

- **3D Models**:
  - `ajimano-sakura-ground.glb`: The main model including the ground, used in `map.html` and `ground.html`.
  - `ajimano-sakura.glb`: A model of a single cherry blossom tree, used in `sakuras.html`.
- **Core Scripts**:
  - `getModelLayer.js`: A module to create a custom 3D model layer for MapLibre GL JS.
  - `mc-controls.js`: Provides Minecraft-style first-person controls for A-Frame scenes.
- **Map Styling**:
  - The map view uses a [custom MapLibre style JSON](https://code4fukui.github.io/vrmap/mapsetting_nobuilding.json) to hide default 3D buildings.

## Dependencies

This project relies on several external libraries loaded via CDN:

- [A-Frame](https://aframe.io/)
- [Three.js](https://threejs.org/)
- [MapLibre GL JS](https://maplibre.org/)

## License

CC BY Open Data by Code for FUKUI / [Digital Twin Echizen Production Executive Committee](https://code4fukui.github.io/digitaltwin/)