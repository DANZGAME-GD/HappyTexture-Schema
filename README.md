# HappyTexture Schema
A JSON Schema specification for defining the UI structure and visual elements in the Geometry Dash Texture Pack Creator. This schema is designed to validate the data structures used for creating layouts, node interactions, and element animations in Geometry Dash.

## 🚀 Key Features
This schema acts as a blueprint for:
* **Hierarchical Structure**: Manages parent-child relationships between elements (e.g., `CCSprite`, `CCMenu`, `CCMenuItemSpriteExtra` etc.)
* **Visual Attributes**: Controls properties such as `position`, `anchor`, `scale`, `rotation`, `skew`, `opacity`, and blending modes
* **Interactivity**: Defines event triggers like `on-click`, `on-hover`, and `on-release` for UI responsiveness.
* **Animations**: Provides definitions for complex actions such as `MoveTo`, `FadeTo`, and `ScaleTo`, with full support for easing functions.
* **Callbacks**: Directly links UI elements to internal application functions (e.g., `onPlay`, `onGarage`, `onOptions`, etc)

## 🛠 Data Structure
This schema uses modular references to maintain consistency:
* **type**: Specifies the Cocos2d-x object being used.
* **attributes**: The primary object for visual configuration and layout management.
* **children**: Enables dynamic nesting of elements, supporting `new`, `query`, `move`, and `index` operations.
* **event**: Handles user actions to ensure UI interactivity.

## 📦 Example
```json
{
    "type": "CCSprite",
    "id": "my-sprite",
    "attributes": {
        "sprite-frame": "GJ_plusBtn_001.png",
        "scale": 0.8,
        "position": {
            "anchor": "top-right",
            "x": -50,
            "y": -50
        }
    }
}
```
For more details, please visit the [Happy Texture wiki](https://github.com/Alphalaneous/HappyTextures/wiki).

## 📝 Contributing
If you would like to suggest new features or report bugs in this schema validation, please open an Issue or submit a Pull Request to this repository.