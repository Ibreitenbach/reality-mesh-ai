# Reality Mesh Apps - Complete Comparison

## 📱 Available Apps

### 1. **reality-mesh-guided.html** ⭐ RECOMMENDED
**Best for**: Optimal data capture with professional techniques

**Features**:
- ✅ 5 guided capture modes (Orbital, Multi-Height, Zoom, Room, Free)
- ✅ Real-time visual guidance with arrows
- ✅ Progress tracking and metrics
- ✅ Rotation tracking (total degrees captured)
- ✅ Speed and movement feedback
- ✅ Sensor data integration
- ✅ Metadata about capture mode and quality

**Use When**: You want the best quality 3D data

---

### 2. **reality-mesh-sensors.html**
**Best for**: Maximum sensor data capture

**Features**:
- ✅ All phone sensors (Gyro, Accel, Magnetometer, GPS, Light)
- ✅ Real-time sensor display
- ✅ Sensor data synchronized with each frame
- ✅ Detailed metadata export
- ✅ No guidance (free capture)

**Use When**: You need comprehensive sensor fusion data

---

### 3. **mesh-capture-standalone.html**
**Best for**: Basic point cloud capture

**Features**:
- ✅ Simple point cloud generation
- ✅ Three.js visualization
- ✅ OBJ export
- ✅ No sensors, no guidance
- ✅ Smallest/simplest app

**Use When**: Quick test or minimal setup

---

## 📊 Quick Comparison

| Feature | Guided | Sensors | Standalone |
|---------|--------|---------|------------|
| **Guidance** | ✅ 5 modes | ❌ | ❌ |
| **Sensors** | ⚠️ Partial | ✅ Full | ❌ |
| **Point Cloud** | ✅ | ✅ | ✅ |
| **Progress Tracking** | ✅ | ⚠️ Basic | ❌ |
| **Setup** | None | None | None |
| **API Required** | ❌ | ❌ | ❌ |
| **File Size** | Medium | Medium | Small |

---

## 🎯 Recommended Workflow

### Best Approach: Hybrid Strategy

#### Option A: Maximum Quality (Guided + Sensors)
1. Use **reality-mesh-guided.html** with "Multi-Height Pro" mode
2. Captures optimal angles with guidance
3. Includes orientation tracking
4. Export includes metadata about capture quality

#### Option B: Maximum Data (Sensors + Manual)
1. Use **reality-mesh-sensors.html**
2. Capture freely with all sensor data
3. Most comprehensive dataset
4. Process later to determine quality

---

## 💡 Capture Mode Recommendations

### For Different Scenarios:

**Small Objects (< 1 foot)**
- App: **reality-mesh-guided.html**
- Mode: **Multi-Height Pro** (3 passes at different heights)
- Time: 2-3 minutes
- Result: Complete 360° coverage

**Medium Objects (1-3 feet)**
- App: **reality-mesh-guided.html**
- Mode: **Quick Orbital** → **Zoom In/Out**
- Time: 1 minute
- Result: Good overall coverage + detail

**Large Objects / Furniture**
- App: **reality-mesh-guided.html**
- Mode: **Quick Orbital** (multiple passes at different distances)
- Time: 2-4 minutes
- Result: All angles captured

**Rooms / Environments**
- App: **reality-mesh-guided.html**
- Mode: **Room Scanner**
- Time: 3-5 minutes
- Result: Complete space documentation

**Quick Tests / Experiments**
- App: **mesh-capture-standalone.html**
- Mode: Free capture
- Time: As needed
- Result: Basic point cloud

---

## 📂 Exported Data Structure

### Guided App Export:
```json
{
  "metadata": {
    "timestamp": "2025-11-05T...",
    "mode": "multi-height",
    "duration": 125.3,
    "frameCount": 150,
    "pointCount": 25000,
    "totalRotation": 720,
    "device": "..."
  },
  "sensors": [ /* orientation data */ ],
  "pointCloud": [ /* x, y, z, r, g, b, frame */ ]
}
```

### Sensors App Export:
```json
{
  "metadata": { /* similar */ },
  "sensors": [
    {
      "frame": 0,
      "timestamp": 123456,
      "orientation": { "alpha": 45, "beta": 12, "gamma": -5 },
      "gyroscope": { "x": 0.1, "y": -0.05, "z": 0.03 },
      "accelerometer": { "x": 0.02, "y": 9.81, "z": 0.15 },
      "magnetometer": { "x": 25.3, "y": -12.1, "z": 45.2 },
      "light": 250,
      "gps": { "lat": 37.77, "lon": -122.41, "alt": 15, "accuracy": 12 }
    }
  ],
  "pointCloud": [ /* same */ ]
}
```

---

## 🚀 Next Steps

### Phase 1: Test Capture ✅ (Current)
- ✅ Apps created
- ⏭️ Test on phone
- ⏭️ Capture sample data

### Phase 2: Process Data
- Build Google Colab notebook
- Clean/optimize point clouds
- Align frames using sensor data
- Generate embeddings

### Phase 3: Build MCP Server
- Store processed meshes
- Enable semantic search
- Claude can query spatial data
- Use for CAD/Blender reference

---

## 📝 Summary

**Start Here**:
1. Open **`reality-mesh-guided.html`** on your phone
2. Try **"Quick Orbital"** mode on a small object
3. Export the JSON
4. Share for processing!

This will give us real data to work with for the next steps! 🎯