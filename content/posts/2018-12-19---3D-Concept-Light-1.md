---
title: Light 1부 _ Ambient, Directional, Hemisphere
date: "2018-12-19T00:00:00.001Z"
template: "post"
draft: false
slug: "3d-concept-light-1"
category: "3D_Concept"
tags:
  - "OpenGL"
  - "Unity"
  - "Unreal"
description: ""
socialImage: "/media/3d-concept_light-1_0.png"
---
![Image]({{ site.url }}/media/3d-concept_light-1_0.jpg)

3D 그래픽스에서 Light의 종류는 Ambient Light, Hemisphere Light, Directional Light와 Point Light, Spot Light 가 있습니다.

굳이 나누는 기준은 **자연광**와 **인조광**으로 나누었습니다.

#### * 3D 그래픽스에서 빛이란?
우리가 눈으로 보는 사물의 색깔은 사물이 빛을 흡수하지 못한 빛을 반사하기 때문에 색이 나타나는 것입니다. 
자연에서 태양에 의해 생성된 빛은 수백, 수만번의 반사를 거쳐 우리에게 전달되는데, 컴퓨터 상에서의의 수백, 수만번의 반사를 수백초분의 1의 시간동안 계산해야 합니다.이것은 실현이 거의 불가능하기 때문에 우리가 볼 수 있는 빛을 조금 더 세분화해서 Preset(프리셋)을 만들어놓고 계산을 실행합니다.

![Image]({{ site.url }}/media/3d-concept_light-1_1.jpg)

#### 1. 환경요소로서의 Light : 자연광
##### a. Ambient Light
Ambient Light(앰비언트 라이트)는 환경광 또는 주변광이라고 하며, 다른 물체에 반사되어 보이는 조명이라는 뜻으로 각종 사전에 적혀있습니다. 하지만 이를 표현하기 위해 가장 비유하기 좋은 상황은, 아주 깜깜한 밤중에 눈을 뜨고 일어나면 아무것도 보이는게 없어야하는데 무엇인가 보인다! 라고 하면 그것이 바로 Ambient Light 입니다. 사실은 그마저도 달에 반사된 햇빛이 비추기 때문에 은은한 빛이 도는 것이지만, 그 마저도 반사를 거친 빛이라면 그냥 Ambient Light의 존재의 필요성을 느끼게 됩니다. 일반적으로 Ambient Light 는 RGB와 Intensity 속성을 가지고 있습니다.

![Image]({{ site.url }}/media/3d-concept_light-1_2.jpg)
분명히 무언가 보이는 사진입니다.

##### b. Directional Light
Directional Light(디렉셔널 라이트)는 직접광 또는 직사광이라고 하며, 태양광처럼 크고 먼 광원에서 나오는 빛을 의미 합니다. 들어오는 빛의 각도가 모두 평행한 빛이라고 하죠. Directional Light와 빛을 받는 평면이 서로 수직이라면, 그 사이에 존재하는 물체의 그림자의 크기는 물체의 크기과 같다고 할 수 있습니다. 일반적으로 Directional Light는 RGB와 Intensity 속성을 가지고 있으고, Shadow와 관련이 있습니다. 속성값으로 그림자를 소프트하게(번짐효과) 처리할 것인지, 하드하게(경계가 명확) 처리할 것인지 선택을 하기도 하며, Cascade를 적용해 거리에 따라 그림자의 해상도도 설정하게 됩니다.

![Image]({{ site.url }}/media/3d-concept_light-1_3.png)

##### + Hemisphere Light
Hemisphere Light(헤미스피어 라이트)는 반구광?? 이라고 하는데, 이는 기본 빛의 요소는 아니지만, 하늘의 색깔과 땅의 색깔을 주변광처럼 적용시키는 역할을 합니다.

Ambient Light와 Directional Light로도 환경요소로서 빛을 충분히 표현할 수 있지만, Javascript WebGL 오픈소스 라이브러리인 threejs에 들어가있는 Light의 한 종류이기도 합니다. Unity로 비교하자면 Environment Reflection 정도로 해석할 수 있겠네요.

![Image]({{ site.url }}/media/3d-concept_light-1_4.png)
