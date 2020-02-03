---
title: Unity3D _ 2018.2 WebGL 업데이트 정보
date: "2018-12-25T02:57:00.000Z"
template: "post"
draft: false
slug: "unity3d_2018_2_webgl"
category: "Unity3D"
tags:
  - "Graphics"
  - "Unity3D"
description: ""
socialImage: ""
---

#### 2018.2

##### * Backwards Compatibility Breaking Changes

WebGL: Allow WebAssembly heap to grow

WebGL: Configured toolchain so it does not generate WebAssembly trapping instructions.

WebGL: Enable Data Caching option in new projects

WebGL: Upgraded toolchain to emscripten 1.37.33 and binaryen 42

WebGL: WebAssembly is the default Linker Target on new projects

##### * Improvements

Editor: Added UWP and WebGL support in the Test Runner

WebGL: Add indexedDB caching support for all build files in WebGL. Add indexedDB caching support for compiled WebAssembly code.

WebGL: Make StreamingAssets path configurable via UnityLoader.instantiate() parameters

##### * Fixed

Web: Fix exception in UnityWebRequest on empty url (981192)

Web: Fix native UnityWebRequest not destroyed until garbage collected even if explicitly disposed (984996)

Web: Fix UnityWebRequest not aborted if Abort() called before sending (977469)

Web: Fix UnityWebRequest with file URIs containing query or fragment (992937)

WebGL: Fix '/b' added to inputString on keyup event (981495)

WebGL: Fix mouse button state after mouse drag (905712)

WebGL: Fix playBuffer exception when there is no audio output on Safari (960863)

WebGL: Fix Webcam support on Firefox and Safari (1005628)

WebGL: Make StreamingAssets path relative to the generated json (951333)

#### * 2018.2.9f

(1057185) - Web: UnityWebRequest: Fixed handling 300 redirect without Location header.

#### * 2018.2.16f

IL2CPP: Add support for CultureInfo in WebGL when exceptions are disabled. (1083520)
