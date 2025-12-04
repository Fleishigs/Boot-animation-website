# Quick Start Guide

## 🚀 Getting Started in 3 Minutes

### 1. Open the Tool
Simply open `index.html` in your browser or visit the [live demo](https://yourusername.github.io/boot-animation-creator/).

### 2. Upload Your Content

**Option A: Images**
- Drag and drop PNG/JPG images onto the upload area
- Or click the upload area to browse files
- Images will appear as frames in order

**Option B: Video**
- Upload any video file (MP4, WebM, etc.)
- The tool automatically extracts frames at your chosen FPS
- Wait for processing to complete

### 3. Configure Settings

```
FPS: 24 (smooth animation, standard)
Loop: 0 (infinite loop)
Resolution: 240x320 (adjust to your device)
```

### 4. Preview
- Click **Play** to see your animation on the flip phone
- Use timeline to scrub through frames
- Click any thumbnail to jump to that frame

### 5. Export
- Click **Export bootanimation.zip**
- File downloads automatically
- Ready to flash to your device!

## 📱 Flashing to Your Device

### Requirements
- Rooted Android device OR
- Custom recovery (TWRP recommended)

### Quick Flash via TWRP
```bash
1. Copy bootanimation.zip to your phone
2. Boot into TWRP recovery
3. Advanced → File Manager
4. Navigate to /system/media/
5. Delete old bootanimation.zip (backup first!)
6. Copy new bootanimation.zip here
7. Set permissions: rw-r--r-- (644)
8. Reboot
```

### Quick Flash via ADB
```bash
adb root
adb remount
adb push bootanimation.zip /system/media/
adb shell chmod 644 /system/media/bootanimation.zip
adb reboot
```

## 💡 Tips

- **Higher FPS = Smoother** but larger file size (24-30 FPS is ideal)
- **Keep it short** - Most boot animations are 3-10 seconds
- **Test resolution** - Match your device's screen resolution
- **Preview first** - Always test before flashing
- **Backup original** - Save your stock bootanimation.zip

## 🎨 Creating Great Animations

1. **Keep frames consistent** - Same resolution for all images
2. **Use transparency** - PNG with alpha looks great
3. **Consider timing** - Too fast = seizure, too slow = boring
4. **Test on phone** - Preview on the flip phone mockup
5. **Compress if needed** - Large files slow boot time

## ⚠️ Troubleshooting

**Animation won't play?**
- Check file permissions (must be 644)
- Verify desc.txt format
- Ensure frames are named correctly (frame00000.png, frame00001.png, etc.)
- Check if /system partition is mounted as read-write

**Stuck at boot?**
- Boot into recovery
- Restore original bootanimation.zip
- Check logcat for errors

**File too large?**
- Reduce resolution
- Lower FPS
- Use fewer frames
- Compress PNG images

## 🔗 Useful Resources

- [XDA Forums - Boot Animations](https://forum.xda-developers.com/)
- [Android Boot Animation Documentation](https://android.googlesource.com/)
- [TWRP Official Site](https://twrp.me/)

---

Need help? Open an issue on GitHub! ⚡
