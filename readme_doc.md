
以下是針對 **A-Frame (WebVR/WebXR 框架)** 的簡易 Cheat Sheet，以繁體中文整理，便於快速查閱：

---

### 🔧 **基本結構**

```html
<html>
  <head>
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <!-- 3D 物件、相機、光源放這裡 -->
    </a-scene>
  </body>
</html>
```

---

### 📦 **常用 Primitive 元件**

| 元件           | 範例                                                  | 描述   |
| ------------ | --------------------------------------------------- | ---- |
| `a-box`      | `<a-box color="red"></a-box>`                       | 立方體  |
| `a-sphere`   | `<a-sphere radius="1.25"></a-sphere>`               | 球體   |
| `a-cylinder` | `<a-cylinder height="1" radius="0.5"></a-cylinder>` | 圓柱體  |
| `a-plane`    | `<a-plane width="4" height="4"></a-plane>`          | 平面   |
| `a-sky`      | `<a-sky color="#ECECEC"></a-sky>`                   | 天空背景 |
| `a-text`     | `<a-text value="Hello"></a-text>`                   | 文字   |

---

### 🎯 **基本屬性**

| 屬性         | 說明     | 範例                                   |
| ---------- | ------ | ------------------------------------ |
| `position` | 位置     | `position="0 1 -3"`                  |
| `rotation` | 旋轉     | `rotation="0 45 0"`                  |
| `scale`    | 縮放     | `scale="2 2 2"`                      |
| `color`    | 顏色     | `color="#FF0000"`                    |
| `material` | 材質     | `material="opacity:0.5"`             |
| `geometry` | 幾何形狀參數 | `geometry="primitive:box; height:2"` |

---

### 📸 **相機與控制**

```html
<a-entity camera look-controls wasd-controls position="0 1.6 0"></a-entity>
```

* `camera`：啟用相機
* `look-controls`：滑鼠/手機轉頭控制
* `wasd-controls`：鍵盤移動（WASD）

---

### 💡 **光源元件**

| 元件        | 範例                                                                |
| --------- | ----------------------------------------------------------------- |
| `a-light` | `<a-light type="ambient" color="#fff"></a-light>`                 |
| 點光源       | `<a-light type="point" intensity="2" position="2 4 4"></a-light>` |

---

### 🖼️ **材質與貼圖**

```html
<a-box src="#texture-id"></a-box>

<a-assets>
  <img id="texture-id" src="texture.jpg">
</a-assets>
```

---

### 🕹️ **互動 (事件)**

```html
<a-box id="myBox" color="blue"></a-box>

<script>
  document.querySelector('#myBox').addEventListener('click', () => {
    alert('被點了！');
  });
</script>
```

---

### 🔁 **動畫 (Animation)**

```html
<a-box animation="property: rotation; to: 0 360 0; loop: true; dur: 2000"></a-box>
```

---

### 📁 **擴充元件範例**

| 功能      | 套件                                              |
| ------- | ----------------------------------------------- |
| 控制器支援   | `aframe-extras`                                 |
| 粒子效果    | `aframe-particle-system-component`              |
| 物理引擎    | `aframe-physics-system`                         |
| glTF 載入 | `<a-gltf-model src="model.glb"></a-gltf-model>` |

---

### 🌐 **資源推薦**

* 官方網站：[https://aframe.io](https://aframe.io)
* A-Frame Registry（元件庫）：[https://aframe.io/aframe-registry](https://aframe.io/aframe-registry/)
* 線上編輯器（Glitch / CodePen）：支援即時預覽

---

若你需要 PDF / 圖表版或想整理成中文教學頁面，我也可以幫你生成！是否需要？
