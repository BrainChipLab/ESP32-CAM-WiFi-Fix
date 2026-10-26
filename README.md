# ESP32-CAM-WiFi-Fix
Code snippets and checklist for fixing ESP32-CAM WiFi connection and streaming issues.


# ESP32-CAM Not Connecting to WiFi — Code & Quick Checklist

Quick config and signal check for the official `CameraWebServer` example (`File -> Examples -> ESP32 -> Camera -> CameraWebServer`).

### 1. Select the Right Board Model (`board_config.h` on Core 3.2.1+ or top of `.ino`)
Make sure **only ONE** camera model is uncommented. The default is `CAMERA_MODEL_ESP_EYE` — change it to `CAMERA_MODEL_AI_THINKER`:

```cpp
// board_config.h (core 3.2.1+) — only ONE model active
//#define CAMERA_MODEL_ESP_EYE  // Has PSRAM
#define CAMERA_MODEL_AI_THINKER // Has PSRAM
