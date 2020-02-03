---
title: Unity3D _ 2018.3 WebGL 업데이트 정보
date: "2018-12-25T03:11:00.000Z"
template: "post"
draft: false
slug: "unity3d_2018_3_webgl"
category: "Unity3D"
tags:
  - "Graphics"
  - "Unity3D"
description: ""
socialImage: ""
---

#### 2018.3

##### * Backwards Compatibility Breaking Changes

Web: WWW is now obsolete. Use UnityWebRequest instead.

WebGL: Added asm.js deprecation warning.

WebGL: Enabled WebAssembly traps in Development builds.

WebGL: Removed caching support for compiled WebAssembly module.

WebGL: Unity no longer uses glGetProcAddress internally.

WebGL: WebAssembly is now the default Linker Target on new WebGL projects.

##### * Improvements

Scripting: Added the status code and name of the error (rather than a generic message) to the error property of UnityWebRequest when it encounters an HTTP error.

Web: UnityWebRequest now supports cookies in the same game session. Added API to remove them.

##### * API Changes

WebGL: Fixed canvas resize when using Linear color space. (977579)

WebGL: Fixed integer overflow on start-up when Performance Reporting is enabled. (1085302)

WebGL: Fixed mouse input simulation when using touch inputs. (970812)

WebGL: Fixed Unity WebGL content termination. Calling Application.Quit() will stop execution.

WebGL: Fixed WebCamTexture device name (894564)

WebGL: Fixed UnityLoader.js memory leak.

WebGL: Replace usage of deprecated WebAudio gain/playbackRate.value with setValueAtTime() (965647)

WebGL: Replace usage of deprecated WebAudio listener setPosition/setOrientation with position/forward/up.setValueAtTime() (1003912)

WebGL: Workaround for audio not working in Chrome (as of version 66) until the user interacts with the page. (1003917)
