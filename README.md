# 🌐 Reality Mesh AI

**3D Spatial Capture Web Apps with Sensor Fusion**

Capture your environment in 3D using just your phone's camera and sensors. No installation required - just open in your browser!

---

## 🚀 Try It Now!

### [🎯 **Guided Capture** (Recommended)](https://ibreitenbach.github.io/reality-mesh-ai/reality-mesh-guided.html)
Professional capture modes with step-by-step guidance

### [📱 **Sensor Fusion**](https://ibreitenbach.github.io/reality-mesh-ai/reality-mesh-sensors.html)
Maximum sensor data (gyro, accelerometer, GPS, compass)

### [✨ **Simple Capture**](https://ibreitenbach.github.io/reality-mesh-ai/mesh-capture-standalone.html)
Quick and easy point cloud capture

---

## ✨ Features

- **5 Professional Capture Modes**: Orbital, Multi-Height, Zoom, Room Scanner, Free
- **Real-Time Guidance**: Visual arrows and progress tracking
- **Full Sensor Suite**: Gyroscope, Accelerometer, Magnetometer, GPS, Ambient Light
- **Export Data**: JSON with point clouds, sensor data, and metadata
- **No Installation**: Works directly in your mobile browser
- **No API Keys**: Everything runs locally

---

## 📱 Quick Start

1. **Open on your phone**: Visit [https://ibreitenbach.github.io/reality-mesh-ai/](https://ibreitenbach.github.io/reality-mesh-ai/)
2. **Choose an app**: Start with [Guided Capture](https://ibreitenbach.github.io/reality-mesh-ai/reality-mesh-guided.html)
3. **Grant permissions**: Allow camera and sensor access
4. **Start capturing**: Follow the on-screen guidance
5. **Export**: Download your 3D data as JSON

---

## 📊 App Comparison

| App | Best For | Time | Sensors | Guidance |
|-----|----------|------|---------|----------|
| **Guided** | Quality 3D capture | 30s-3min | Partial | ✅ 5 modes |
| **Sensors** | Max sensor data | Any | ✅ Full | ❌ |
| **Standalone** | Quick tests | 15s+ | ❌ | ❌ |

[Full Comparison Guide →](./APP-COMPARISON.md)

---

## 🎯 Capture Techniques

Different patterns produce different quality results:

- **Orbital**: Circle around object (best for small objects)
- **Multi-Height**: Multiple circles at different heights (best quality)
- **Zoom In/Out**: Move toward/away from object (depth focus)
- **Room Scanner**: Grid pattern for environments
- **Free Capture**: Manual control

[Complete Technique Guide →](./CAPTURE-TECHNIQUES.md)

---

## 📂 Exported Data

Each capture exports a JSON file with:

```json
{
  "metadata": {
    "timestamp": "2025-11-05T...",
    "mode": "orbital",
    "duration": 45.2,
    "frameCount": 120,
    "pointCount": 15000,
    "totalRotation": 360
  },
  "sensors": [ /* orientation, gyro, accel, GPS... */ ],
  "pointCloud": [ /* x, y, z, r, g, b, frame */ ]
}
```

---

## 🔧 Technical Details

- **Built With**: Vanilla JavaScript, Three.js, HTML5 Sensors API
- **Browser Support**: Chrome/Edge (Android), Safari (iOS with permissions)
- **Depth Estimation**: Brightness-based (MediaPipe integration coming soon)
- **File Format**: JSON with point cloud and sensor data

---

## 🚧 Roadmap

- [ ] MediaPipe integration for real depth sensing
- [ ] WebXR AR mode
- [ ] Direct Google Drive upload
- [ ] Real-time 3D preview
- [ ] Point cloud to mesh conversion
- [ ] MCP server for Claude AI integration

---

## 📖 Documentation

- [App Comparison](./APP-COMPARISON.md) - Which app to use and when
- [Capture Techniques](./CAPTURE-TECHNIQUES.md) - Professional scanning patterns
- [Sensor Guide](./SENSOR-README.md) - Understanding sensor data

---

## 🎓 Use Cases

- **3D Scanning**: Capture objects for 3D modeling
- **Spatial AI**: Train AI with real-world spatial data
- **AR/VR**: Create assets for immersive experiences
- **Documentation**: Record environments and objects
- **Research**: Collect sensor + visual datasets

---

## 🤝 Contributing

This is an experimental project exploring spatial AI and 3D capture techniques. Feel free to fork and experiment!

---

## 📝 License

MIT License - Feel free to use and modify!

---

**Built with Claude Code** 🤖