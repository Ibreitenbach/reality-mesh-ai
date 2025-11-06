# Optimal 3D Capture Techniques

## Overview
Different capture patterns produce different quality results. This guide covers professional photogrammetry and 3D scanning techniques.

---

## 🎯 Capture Patterns

### 1. **Orbital Capture** (Best for Objects)
**Pattern**: Circle around object at constant distance

**Steps**:
1. Position object in center of clear space
2. Start at eye-level, 3-5 feet away
3. Walk in complete circle (360°) around object
4. Keep camera pointed at object center
5. Move smoothly, no jerky movements
6. Capture 1-2 seconds of video per 10° of rotation

**Best For**:
- Small to medium objects (chair, sculpture, person)
- Objects you can walk around
- Centered subjects

**Data Quality**: ⭐⭐⭐⭐⭐
- Excellent coverage from all angles
- Consistent distance = consistent depth
- Easy to align frames (predictable motion)

**Sensor Benefits**:
- Gyroscope tracks rotation rate
- Magnetometer provides absolute heading
- Consistent accelerometer readings

---

### 2. **Multi-Height Orbital** (Best Quality Overall)
**Pattern**: Multiple circles at different heights

**Steps**:
1. **Low orbit** (knee level) - circle object
2. **Mid orbit** (eye level) - circle object
3. **High orbit** (overhead angle) - circle object
4. Optional: Very low (ground level) and top-down

**Best For**:
- Complex objects with top/bottom features
- Sculptures, furniture, architectural elements
- When you need complete 3D coverage

**Data Quality**: ⭐⭐⭐⭐⭐+
- Complete surface coverage
- No missing data on top/bottom
- Best for reconstruction

**Time**: 2-4 minutes per object

---

### 3. **Zoom In/Out** (Depth Mapping)
**Pattern**: Move toward/away from subject along single axis

**Steps**:
1. Start 10+ feet away
2. Slowly walk toward object (2-3 seconds)
3. Stop very close (1-2 feet)
4. Optionally reverse (walk backward)
5. Keep camera centered on same point

**Best For**:
- Understanding scale/depth
- Single-object focus
- Quick captures
- Testing depth accuracy

**Data Quality**: ⭐⭐⭐
- Good depth information
- Poor side coverage
- Missing angles

**Sensor Benefits**:
- Accelerometer shows approach speed
- Consistent GPS coordinates
- Clear depth gradient

---

### 4. **Grid Sweep** (Best for Rooms/Environments)
**Pattern**: Systematic sweep of entire space

**Steps**:
1. Start at corner of room
2. Pan slowly left-to-right (like reading)
3. Step forward, pan right-to-left
4. Continue in rows until room covered
5. Capture all 4 walls + ceiling + floor

**Best For**:
- Rooms and interior spaces
- Large environments
- Architectural documentation
- Scene understanding

**Data Quality**: ⭐⭐⭐⭐
- Complete room coverage
- Good for floor plans
- Spatial relationships clear

**Time**: 3-5 minutes per room

---

### 5. **Hero Shot + Details** (Hybrid Approach)
**Pattern**: Overall context + close-up details

**Steps**:
1. **Wide shot**: Capture entire scene (orbit or grid)
2. **Medium shots**: Important objects/features
3. **Close-ups**: Detailed textures, labels, specific features
4. **Context shots**: How objects relate to each other

**Best For**:
- Complex scenes with important details
- Documentation + 3D reconstruction
- When you need both context and detail

**Data Quality**: ⭐⭐⭐⭐⭐
- Multi-resolution data
- Context + detail
- Good for semantic understanding

---

## 📊 Comparison Table

| Technique | Object | Room | Speed | Detail | Coverage |
|-----------|--------|------|-------|--------|----------|
| Orbital | ⭐⭐⭐⭐⭐ | ⭐ | Fast | Medium | Good |
| Multi-Height | ⭐⭐⭐⭐⭐ | ⭐⭐ | Slow | High | Excellent |
| Zoom In/Out | ⭐⭐⭐ | ⭐ | Very Fast | High | Poor |
| Grid Sweep | ⭐ | ⭐⭐⭐⭐⭐ | Medium | Medium | Excellent |
| Hero + Details | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | Slow | Excellent | Excellent |

---

## 🎬 Movement Guidelines

### Speed
- **Optimal**: 0.5-1 foot per second
- **Too Fast**: Motion blur, missed frames
- **Too Slow**: Redundant data, large files

### Smoothness
- Use both hands on phone
- Walk heel-to-toe for stability
- Breathe steadily (breath affects stability)
- Stop briefly at key angles

### Frame Overlap
- **Ideal**: 70-80% overlap between frames
- More overlap = easier alignment
- Less overlap = faster capture

---

## 📐 Distance Guidelines

| Object Size | Starting Distance | Ending Distance |
|-------------|------------------|-----------------|
| Small (<1ft) | 2-3 feet | 6 inches |
| Medium (1-3ft) | 5-6 feet | 2 feet |
| Large (>3ft) | 10+ feet | 3-4 feet |
| Room | All walls | N/A |

---

## 💡 Pro Tips

### Lighting
1. **Even lighting** is more important than bright lighting
2. Avoid direct sunlight (harsh shadows)
3. Overcast days are ideal for outdoor capture
4. Use multiple light sources indoors

### Camera Settings
1. Keep focus locked (tap to focus, hold)
2. Exposure locked if possible
3. Avoid zoom - move physically instead
4. Keep phone in landscape mode

### Common Mistakes to Avoid
❌ Moving too fast
❌ Jerky/unsteady movements
❌ Poor lighting with strong shadows
❌ Missing top/bottom angles
❌ Too close (out of focus)
❌ Reflective surfaces (mirrors, glass)
❌ Moving objects in frame

---

## 🧪 Experimental Techniques

### 1. **Spiral Approach**
- Combine zoom-in with orbital
- Walk in spiral getting closer as you circle
- Best of both techniques

### 2. **Figure-8 Pattern**
- Walk figure-8 around object
- Natural variation in angles
- Good for organic subjects

### 3. **Random Walk with Coverage**
- Free-form movement
- Ensure all angles covered
- Good for exploration/testing

---

## 🎯 Recommended Workflow for Our App

### Phase 1: Quick Scan (30 seconds)
1. Single orbital pass at eye level
2. Capture sensor data for orientation
3. Fast preview of object

### Phase 2: Detailed Scan (2-3 minutes)
1. Multi-height orbital (3 passes)
2. Close-up details
3. Full sensor + visual data

### Phase 3: Environment Context (1 minute)
1. Step back for wide shot
2. Show object in environment
3. Spatial relationships

**Total Time**: 3-4 minutes for complete capture

---

## 📱 App Features to Build

### Capture Modes
1. **Quick Orbital** - Guided circle with progress indicator
2. **Pro Multi-Pass** - Multiple heights with guidance
3. **Room Scanner** - Grid pattern guide
4. **Free Capture** - No guidance, just record

### Real-Time Feedback
- Coverage map (which angles captured)
- Movement speed indicator
- Overlap percentage
- Quality metrics (blur detection)

### Guidance System
- Visual overlay showing where to move
- Audio cues ("move left", "move higher")
- Progress indicators
- Vibration feedback for good frames

This will help users capture optimal data without training! 🚀
