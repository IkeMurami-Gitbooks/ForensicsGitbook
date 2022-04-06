---
description: Пример использования ffmpeg
---

# FFMPEG

```
wav (8kHZ bitrate) -> opu
ffmpeg -i pc.wav -ar 48000 -ac 2 -acodec libopus -ab 256k man.opus
```
