---
title: Camera(카메라) _ Perspective & Orthogonal
date: "2018-12-18T00:00:00.001Z"
template: "post"
draft: false
slug: "3d-concept-camera-1"
category: "3D_Concept"
tags:
  - "OpenGL"
description: ""
socialImage: "/media/3d-concept_camera_0.png"
---
![Image]({{ site.url }}/media/3d-concept_camera_0.png)

#### 1. 카메라(Camera)란?
  카메라는 일반적으로 우리가 사진촬영을 위한 광학 기기로 알고 있습니다.<br />
  하지만 3D 그래픽스에서 설명하는 카메라는 가상의 3D 공간에서 어떤 지점을 바라보는 눈입니다.<br />
  즉, 가상공간에 존재하는 가상의 눈을 의미합니다.

#### 2. 카메라의 종류
  3D 공간에서 카메라의 종류는 `Perspective Camera`와 `Orthogonal Camera`가 있습니다.

  ![Image]({{ site.url }}/media/3d-concept_camera_1.png)

##### (1) Perspective Camera : 원근감 있는 카메라<br />
  - Perspective Camera는 가까이 있는 물체는 크게, 멀리 있는 물체는 작게 보이는 원근감이 느껴지는 카메라입니다.
  - 같은 말로 Perspective projection 가 있습니다.
  - Field of View (FOV) : [4. Field of View][4]에서 설명

##### (2) Orthogonal Camera : 정사영(직각의) 카메라
  - Orthogonal Camera는 가까이 있는 물체든, 멀리 있는 물체든 같은 크기로 보이는 카메라입니다.
  - 같은 말로 Orthographic projection, Orthographic Camera, Isometric Camera 가 있습니다.
  - Orthographic Size : [5. Orthographic Size][5]에서 설명

```
*Projection(투영)이란?

3D 물체를 2D 평면위에 투과/투영시키는 것입니다.
우리 눈은 어떤 물체가 망막에 2D 이미지로 맺혀야 보입니다.
카메라도 마찬가지로 센서에 2D 이미지로 맺혀야 보입니다.
즉, 우리는 3D 공간에서 2D 상에 맺힌 이미지를 보고 있는 것입니다.
따라서 3D 가상 공간은 카메라에게서 가까운 2D 평면에 이미지로 투영되어 화면에 보여집니다.
```

#### 3. View Frustum (+ Near plane, Far plane )

![Image]({{ site.url }}/media/3d-concept_camera_2.png)

- Frustum 이란 사각뿔에서 머리가 잘린 절두체를 의미합니다.
- `View Frustum`은 Camera가 보는 시야 안쪽의 Near Plane과 Far Plane으로 잘린 공간을 말합니다.
- `View Frustum`은 `Frustum Culling` 이라고도 하는데, Frustum을 통해 보여지는 공간을 잘랐다는 의미입니다.
- `View Frustum` 바깥의 파란 정사면체는 실제로 화면에 보이지 않을 것이고, 파란 정사면체만 화면에 보일 것입니다.
- 만약! 카메라에서 Near Plane보다 가까운 지점에 물체가 놓이게 된다면 잘려서 보이지 않게 됩니다. 예를 들어, 옛날 서든어택 상자 버그가 활황하던 시절에 상자를 뚫는데 갑자기 모서리부분부터 뚫린것 처럼 보인다! 그것이 Near Plane에 의해 앞부분이 잘려서 안 보이는 현상입니다. 반대로 Far Plane에 잘려서 멀리 있는것이 안 보이게 되는 현상도 존재합니다.

#### 4. Field of View(FOV)
- Perspective Camera 에서만 사용 가능
- FOV는 화각을 말하는 것으로 가까이 보이는 것과 멀리 보이는 것이 아닌!!! 내 양옆으로 얼마나 많은 것을 볼 수 있는지를 의미하는 각도입니다.
- 숫자가 작을수록 좁은 영역을, 숫자가 클수록 넓은 영역을 볼 수 있습니다.
- 일반적인 사람의 FOV는 한 쪽 눈당 60도 입니다. 양쪽 눈의 FOV를 합했을 때는 114~120도 사이입니다. 겹치는 구간이 존재하기 때문이지요.

![Image]({{ site.url }}/media/3d-concept_camera_3.jpg)
![Image]({{ site.url }}/media/3d-concept_camera_4.jpg)

#### 5. Orthographic Size
- Orthogonal Camera 에서만 사용 가능
- Orthographic Size는 Zoom Level이 의미하는 것과 비슷한데, 숫자가 작을수록 가까운 곳에서 확대되어 보이고, 숫자가 클수록 먼 곳에서 축소되어 보이는 것입니다.

[4]: #
[5]: #
