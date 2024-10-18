# Three-js-Journey
These are the learning notes of [Three.js Journey](https://threejs-journey.com/) Lessons by Bruno Simon

## 1 Introduction

### 1.1 Setup
Vite: local server

Node.js: environment that runs Javascript outsied Web

### 1.2 Transformation

### 1.3 Animations

### 1.4 Cameras

### 1.5 Viewport 

#### 1.5.1 Resize
```
window.addEventLisener('resize', () => {})
```
#### 1.5.2 Full screen

### 1.6 GUI
```
import GUI from 'lil-gui'
const gui = new GUI()
```

### 1.7 Textures

## 2 Shaders
### 2.1 Variables
**Uniforms** are variables that have the same value for all vertices

**Attributes** are variables associated with each vertex

**Varyings** are variables that are passed from the vertex shader to the fragment shader

### 2.2 Vertex Shader
```
uniform mat4 projectionMatrix;
uniform mat4 viewMatrix;
uniform mat4 modelMatrix;

attribute vec3 position;

void main()
{
  gl_Position = projectionMatrix * viewMatrix * modelMatrix * vec4(position, 1.0);
}
```
### 2.3 Fragment Shader
```
precision mediump float;

void main()
{
  gl_FragColor = vec4(1.0, 0.0, 0.0, 1.0);
}
```

