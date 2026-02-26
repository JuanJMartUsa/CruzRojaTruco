# CruzRojaTruco

A starter Unity 6 project for a 3D Universal (URP) videogame.

## Requirements

- **Unity 6000.0.30f1** (Unity 6)
- Universal Render Pipeline (URP) 17.0.3

## Project Structure

```
Assets/
  Scenes/
    MainMenu.unity   – Title / main menu scene
    GameScene.unity  – Primary gameplay scene
  Scripts/
    SceneLoader.cs   – Helper MonoBehaviour for scene transitions
  Settings/
    UniversalRenderPipelineAsset.asset  – URP pipeline asset
Packages/
  manifest.json      – Unity package dependencies
ProjectSettings/     – Unity project settings
```

## Scenes

| Scene | Description |
|-------|-------------|
| **MainMenu** | Entry-point scene with a title text canvas, directional light and main camera. |
| **GameScene** | Gameplay scene with a ground plane, directional light and main camera. |

## Getting Started

1. Open the project in **Unity 6000.0.30f1** or later (Unity 6 series).
2. Unity will resolve all packages from `Packages/manifest.json` automatically.
3. Open `Assets/Scenes/MainMenu.unity` to start editing the main menu.
4. Use `SceneLoader.LoadGameScene()` (or a UI button event wired to it) to transition to the gameplay scene.

## Scene Transitions

`Assets/Scripts/SceneLoader.cs` exposes convenient methods:

```csharp
sceneLoader.LoadMainMenu();   // go to MainMenu
sceneLoader.LoadGameScene();  // go to GameScene
sceneLoader.QuitGame();       // quit (or stop Play Mode in the Editor)
```
