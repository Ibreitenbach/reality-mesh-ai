# Reality Mesh AI with Sensor Fusion

Complete spatial capture combining camera + all phone sensors.

## Files

- **`reality-mesh-sensors.html`** - Full sensor + visual capture (RECOMMENDED)
- **`reality-mesh-local.html`** - Visual only with simple object detection
- **`mesh-capture-standalone.html`** - Basic 3D point cloud capture

## Captured Data

### Visual
- Camera frames (environment camera)
- 3D point cloud with RGB colors
- Depth estimation from brightness

### Sensors
- **Device Orientation** (compass heading, tilt)
- **Gyroscope** (rotation rates)
- **Accelerometer** (movement, gravity)
- **Magnetometer** (magnetic field, absolute direction)
- **GPS** (location, altitude, accuracy)
- **Ambient Light** (illuminance in lux)

## Usage

1. **Copy to Phone**: Transfer `reality-mesh-sensors.html` to your Samsung Galaxy S24 FE
2. **Open in Chrome**: Use Chrome for best sensor support
3. **Grant Permissions**: Allow camera, location, and sensor access
4. **Start Capture**: Move phone around to scan environment
5. **Export**: Download JSON with all captured data

## Exported Data Format

```json
{
  "metadata": {
    "timestamp": "2025-11-05T...",
    "device": "...",
    "frameCount": 120,
    "pointCount": 15000,
    "sensorSamples": 120,
    "duration": 4.5
  },
  "sensors": [
    {
      "frame": 0,
      "timestamp": 1730842800000,
      "orientation": { "alpha": 45.2, "beta": 12.3, "gamma": -5.1 },
      "gyroscope": { "x": 0.12, "y": -0.05, "z": 0.03 },
      "accelerometer": { "x": 0.02, "y": 9.81, "z": 0.15 },
      "magnetometer": { "x": 25.3, "y": -12.1, "z": 45.2 },
      "light": 250,
      "gps": { "lat": 37.7749, "lon": -122.4194, "alt": 15.2, "accuracy": 12.5 }
    }
  ],
  "pointCloud": [
    { "x": 1.2, "y": -0.5, "z": -1.8, "r": 0.8, "g": 0.6, "b": 0.4, "frame": 0 }
  ]
}
```

## Next Steps

### 1. Process in Google Colab
- Upload exported JSON
- Clean/optimize point cloud
- Generate semantic embeddings
- Align frames using sensor data (SLAM)

### 2. Store in Local MCP Server
- Searchable mesh library
- Claude can query spatial data
- Use for CAD/Blender reference

### 3. Sensor Fusion Applications
- **SLAM** (Simultaneous Localization and Mapping) using gyro + accel
- **Compass alignment** for world-space coordinates
- **GPS tagging** for outdoor captures
- **Lighting analysis** for realistic rendering

## Sensor Support by Browser

| Sensor | Chrome Android | Safari iOS |
|--------|---------------|------------|
| Orientation | ✅ | ✅ |
| Gyroscope | ✅ | ✅ (with permission) |
| Accelerometer | ✅ | ✅ (with permission) |
| Magnetometer | ⚠️ Limited | ⚠️ Limited |
| GPS | ✅ | ✅ (with permission) |
| Ambient Light | ⚠️ Limited | ❌ |

## Tips for Best Results

1. **Lighting**: Use well-lit environments for better depth estimation
2. **Movement**: Move slowly and steadily for better tracking
3. **Calibration**: Hold phone steady for 1-2 seconds before starting
4. **Battery**: Sensor + camera use is intensive - keep charger nearby
5. **Permissions**: Grant all permissions for full sensor access

## Why This Matters for Claude

With sensor-enriched mesh data, I can:
- Understand spatial relationships better
- Generate more accurate CAD models
- Provide context-aware 3D design suggestions
- Learn real-world object proportions
- Build a semantic 3D memory system

This is the foundation for true spatial AI! 🚀
