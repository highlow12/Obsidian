---
title: "모바일 게임 성능 최적화: 물리, UI, 오디오 설정에 대한 전문가 팁"
source: "https://unity.com/kr/blog/games/optimize-your-mobile-game-performance-get-expert-tips-on-physics-ui-and-audio-settings"
author:
  - "[[Unity]]"
published:
created: 2024-11-26
description: "Integrated Success 팀은 유니티 고객들이 복잡한 기술적 문제를 해결할 수 있도록 지원합니다. 유니티의 선임 소프트웨어 엔지니어로 구성된 이 팀과 함께 모바일 게임 최적화에 관한 전문적인 지식을 공유하는 자리를 마련했습니다."
tags:
  - "clippings"
---
Integrated Success 팀은 유니티 고객들이 복잡한 기술적 문제를 해결할 수 있도록 지원합니다. 유니티의 선임 소프트웨어 엔지니어로 구성된 이 팀과 함께 모바일 게임 최적화에 관한 전문적인 지식을 공유하는 자리를 마련했습니다.

유니티의 엔진 소스 코드를 완벽하게 파악하고 있는 [Accelerate Solutions](https://unity.com/kr/success-plans) 팀은 Unity 엔진을 최대한 활용할 수 있도록 수많은 고객을 지원합니다. 팀은 크리에이터 프로젝트를 심도 있게 분석하여 속도, 안정성, 효율성 등을 향상시키기 위해 최적화할 부분을 파악합니다.

모바일 게임 최적화에 관한 인사이트를 공유하기 시작하면서, 원래 계획한 하나의 블로그 포스팅에 담기에는 너무나 방대한 정보가 있다는 사실을 알게 되었습니다. 따라서 이 방대한 지식을 한 권의 전자책([여기](https://create.unity3d.com/optimize-mobile-game-eBook)에서 다운로드 가능)과 75가지 이상의 실용적인 팁을 담은 블로그 포스팅 시리즈를 통해 제공하기로 했습니다.

이번 시리즈의 두 번째 포스팅에서는 UI, 물리, 오디오 설정을 통해 성능을 개선하는 방법을 자세히 살펴봅니다. [이전 포스팅](https://blog.unity.com/kr/technology/optimize-your-mobile-game-performance-tips-on-profiling-memory-and-code-architecture)에서는 프로파일링, 메모리, 코드 아키텍처에 대해 다뤘으며, 다음 포스팅에서는 에셋, 프로젝트 구성, 그래픽스에 대해 다룰 예정입니다.

시리즈 전체 내용을 지금 바로 확인하고 싶다면 무료로 [전자책](https://create.unity3d.com/optimize-mobile-game-eBook)을 다운로드하세요.

그럼 시작하겠습니다.

물리

Unity의 빌트인 물리(Nvidia PhysX)를 모바일에서 사용하려면 많은 리소스가 소요될 수 있지만, 다음 팁을 참고하면 초당 프레임 수를 늘릴 수 있습니다.

설정 최적화

가능하다면 항상 [PlayerSettings](https://docs.unity3d.com/2018.2/Documentation/Manual/class-PlayerSettings.html)에서 **Prebake Collision Meshes**를 선택합니다.

![Image of the in player settings box with a dark grey background and the text "prebake collision meshes*" checked and squared off in red](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2F2ccee6bfbf837ac3dd5fcddec537aefeef1838a1-1198x466.png&w=3840&q=75)

가능하다면 항상 **물리 설정**(**Project Settings > Physics**)을 편집하여 **Layer Collision Matrix**를 단순화합니다.

**Auto Sync Transforms**를 비활성화하고 **Reuse Collision Callbacks**를 활성화합니다.

![Picture of the project settings box with a grey background and the sections for "Auto Sync Transforms" and "Layer Collision Matrix" squared off in red.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Fb5246c66a60c7bdc84ef5b3c660cae6a93b46fec-1712x1999.png&w=3840&q=75)

![Image of the physics module of the profiler with the 5ms section showing activity in green, blue, and orange against a black background.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Ffbb3a3d19242fafe992b504f4ee13db438243574-1999x751.png&w=3840&q=75)

콜라이더 단순화

메시 콜라이더는 많은 리소스를 요합니다. 복잡한 메시 콜라이더를 기본 또는 단순화된 메시 콜라이더로 대체하여 원래 모양을 대략적으로 표현하세요.

![Use primitives or simplified meshes for colliders.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Fdf39525dfa9daa33c4a6464fbd7bc192d706ba3d-1999x1805.png&w=3840&q=75)

물리 메서드를 사용하여 리지드바디 이동

**MovePosition** 또는 **AddForce**와 같은 클래스 메서드를 사용하면 **Rididbody** 오브젝트를 이동할 수 있습니다. **트랜스폼** 컴포넌트를 직접 변환하면 물리 월드에서 다시 계산하게 되어, 복잡한 씬의 경우 리소스를 많이 소모합니다. **Update** 대신 **FixedUpdate**에서 물리 바디를 이동시킵니다.

Fixed Timestep 고정

Project Settings에서 **Fixed Timestep**의 기본값은 0.02(50Hz)입니다. 이를 목표 프레임 속도와 일치하도록 변경합니다(예: 30fps는 0.03).

만약 런타임에서 프레임 속도가 하락하면 Unity가 프레임당 **FixedUpdate**를 여러 번 호출하게 되어 물리가 많이 사용된 콘텐츠에서 CPU 성능 문제를 유발할 수 있습니다.

**Maximum Allowed Timestep**은 프레임 속도가 하락하는 경우 물리 계산 및 FixedUpdate 이벤트가 사용할 수 있는 시간의 양을 제한합니다. 이 값을 낮추면 성능 문제 발생 시 물리 및 애니메이션이 느려지도록 하여 프레임 속도에 미치는 영향을 줄일 수 있습니다.

![Image of the fixed time module inside the project settings with a grey background and white text.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Fb2d79f7c8051794b4bb27ce4db06b4648b30da62-883x235.jpg&w=3840&q=75)

Physics Debugger를 통한 시각화

Physics Debug 창(**Windows > Analysis > Physics Debugger**)을 사용하면 콜라이더나 불일치로 인한 문제를 해결할 수 있습니다. 이 창은 서로 충돌할 수 있는 게임 오브젝트를 색으로 구별하여 표시합니다.

![Image of an orange boat with a mesh overlay and a blue shadow inside the physics debugger dialog box.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Ffa8747e085a83b9726c88514235373bee7517dea-1999x1133.png&w=3840&q=75)

자세한 내용은 Unity 기술 자료의 [Physics Debug Visualization](https://docs.unity3d.com/Manual/PhysicsDebugVisualization.html)을 참조하세요.

사용자 인터페이스

UGUI([Unity UI](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/index.html?utm_source=demand-gen&utm_medium=pdf&utm_campaign=asset-links-gmg-elevate-your-game&utm_content=optimize-mobile-game-performance-ebook))는 성능 문제의 원인이 되는 경우가 많습니다. Canvas 컴포넌트는 UI 요소에 대한 메시를 생성 및 업데이트하고 GPU에 드로우 콜을 보냅니다. 이러한 기능은 리소스를 많이 소모할 수 있으므로 UGUI를 사용할 때 다음 사항을 기억하세요.

Canvas 나누기

수천 개의 요소가 포함된 하나의 대형 Canvas에서는 UI 요소를 하나만 업데이트해도 전체 Canvas가 강제로 업데이트되므로 CPU 스파이크가 발생할 수 있습니다.

다수의 Canvas를 지원하는 UGUI의 기능을 활용하세요. 새로 고침해야 하는 빈도에 따라 UI 요소를 나눕니다. 정적 UI 요소는 별도의 Canvas에 두고, 동시에 업데이트되는 동적 요소는 보다 작은 하위 Canvas에 둡니다.

각 Canvas 내의 모든 UI 요소가 동일한 Z 값, 머티리얼, 텍스처를 갖도록 해야 합니다.

보이지 않는 UI 요소 숨기기

게임에서 간헐적으로만 나타나는 UI 요소(예: 캐릭터가 대미지를 입었을 때 나타나는 체력 표시줄)가 있을 수 있습니다. 보이지 않는 UI 요소가 활성화된 경우에도 드로우 콜을 사용할 수 있습니다. 보이지 않는 UI 컴포넌트를 명시적으로 비활성화하고 필요할 때 다시 활성화합니다.

Canvas의 가시성만 해제하면 되는 경우 게임 오브젝트 대신 Canvas 컴포넌트를 비활성화합니다. 이렇게 하면 메시와 버텍스를 재구성하지 않아도 됩니다.

GraphicRaycaster를 제한하고 Raycast Target 비활성화하기

**GraphicRaycaster** 컴포넌트는 화면 터치나 클릭과 같은 입력 이벤트에 필요합니다. 이 컴포넌트는 화면의 각 입력 지점을 순환하며 입력 지점이 UI의 RectTransform 내에 있는지 확인합니다.

계층 구조의 맨 위쪽 Canvas에서 기본 **GraphicRaycaster**를 제거하세요. 대신, 상호 작용이 필요한 개별 요소(버튼, Scrollrect 등)에만 **GraphicRaycaster**를 추가합니다.

![Image of the grey graphic raycaster dialog box with white text.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Fdad8ae8ce858a092ebd1356cddebc2568d5c9357-685x171.jpg&w=3840&q=75)

아울러 모든 UI 텍스트 및 이미지에서 불필요하게 활성화된 **Raycast Target**도 비활성화합니다. UI에 많은 요소가 있어 복잡한 경우 이와 같이 간단히 설정을 변경하여 불필요한 계산을 줄일 수 있습니다.

![Image dialog box with a grey background and the text "Raycast Target" outlined in a red square.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2Fbdae8b2bc55c7d98de5ac6dee149d0feaccc8c35-787x309.png&w=3840&q=75)

Layout Group

Layout Group은 비효율적으로 업데이트되므로 반드시 필요할 때만 사용하세요. 콘텐츠가 동적이지 않은 경우 Layout Group을 아예 사용하지 말고, 비율 레이아웃에 앵커를 대신 사용하시기 바랍니다. 그 밖의 경우에는 UI 설정을 마친 후 커스텀 코드를 생성하여 [Layout Group](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/UIAutoLayout.html?utm_source=demand-gen&utm_medium=pdf&utm_campaign=asset-links-gmg-elevate-your-game&utm_content=optimize-mobile-game-performance-ebook) 컴포넌트를 비활성화합니다.

동적 요소에 Layout Group(Horizontal, Vertical, Grid)을 사용해야 하는 경우, 중첩되지 않도록 하여 성능을 개선합니다.

![Grid layout group dialog box with grey background and white text.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2F49138bd7850c4f110437bc88a6c9f632dfb5d2ca-685x261.jpg&w=3840&q=75)

대형 리스트 뷰와 그리드 뷰 사용 시 주의

대형 리스트 뷰와 그리드 뷰는 많은 리소스를 소모합니다. 대형 리스트 또는 그리드 뷰(예: 수백 개의 항목이 있는 인벤토리 화면)를 만들어야 하는 경우 항목마다 UI 요소를 만드는 대신 소규모 UI 요소의 풀을 재사용하는 것이 좋습니다. 샘플 [GitHub 프로젝트](https://github.com/boonyifei/ScrollList)를 통해 실제 작동 모습을 확인하세요.

요소의 과도한 레이어링 주의

다수의 UI 요소를 레이어링하면(예: 카드 시합 게임에서 쌓여 있는 카드) 오버드로우가 발생합니다. 코드를 커스터마이즈하여 런타임에 레이어링된 요소를 병합하여 요소나 배치(batch)의 수를 줄이세요.

다양한 해상도 및 종횡비 사용

현재 모바일 기기에서 사용 중인 해상도와 화면 크기가 매우 다양하므로, 각 기기에서 최상의 경험을 제공하는 [대체 버전의 UI](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/HOWTO-UIMultiResolution.html)를 만드세요.

[Device Simulator](https://docs.unity3d.com/Manual/com.unity.device-simulator.html)를 사용하여 지원되는 다양한 기기의 UI를 미리 볼 수 있습니다. [XCode](https://developer.apple.com/library/archive/documentation/IDEs/Conceptual/iOS_Simulator_Guide/GettingStartedwithiOSSimulator/GettingStartedwithiOSSimulator.html#//apple_ref/doc/uid/TP40012848-CH5-SW10)와 [Android Studio](https://developer.android.com/studio/run/managing-avds)에서 가상 기기를 만들 수도 있습니다.

![Image of the device simulator that has a grey dialog box background and a simulation of a racing boat game on a smartphone.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2F7200a48809d5e642df6cfca0e1e7ef25e37e3191-1552x784.jpg&w=3840&q=75)

전체 화면 UI 사용 시 기타 요소 모두 숨기기

일시 중지 화면이나 시작 화면이 씬의 나머지 부분을 모두 가리는 경우, 3D 씬을 렌더링하는 카메라를 비활성화합니다. 마찬가지로 맨 위쪽 Canvas에 가려진 배경 Canvas 요소도 모두 비활성화합니다.

60fps에서는 업데이트할 필요가 없으므로 전체 화면 UI 사용 시에는 **Application.targetFrameRate**를 낮게 설정하는 것이 좋습니다.

World Space 및 Camera Space Canvas 카메라 설정

**Event** 또는 **Render Camera** 필드를 공백으로 두면 Unity가 자동으로 **Camera.main**을 채워 넣어 불필요한 리소스가 소모됩니다.

가능한 경우 Canvas의 **RenderMode**에 카메라가 필요 없는 **Screen Space – Overlay**를 사용하는 것이 좋습니다.

![Image of the Camera space canvases dialog box with a greyed out background and white text.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2F9f1666be36ab05be5fdf10ad6a0abbeebe5e086b-687x208.jpg&w=3840&q=75)

오디오

오디오는 일반적인 성능 저하 원인은 아니지만 최적화를 통해 메모리를 절약할 수 있습니다.

![Inspector dialog box with grey background and white text with an orange voice modulator at the bottom.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2F2b45cb3a63a5c9ef98dc4956419eab6a7aca4941-576x1063.jpg&w=3840&q=75)

가능한 경우 압축되지 않은 원본 WAV 파일을 소스 에셋으로 사용

압축된 형식(예: MP3 또는 Vorbis)을 사용하는 경우 Unity에서 압축을 푼 뒤 빌드 시간 동안 재압축해야 합니다. 그 결과 손실이 두 번 발생하여 최종 품질이 저하됩니다.

클립을 압축하고 압축 비트레이트 낮추기

압축을 통해 클립의 크기와 메모리 사용량을 줄이세요.

- 대부분의 사운드에 **Vorbis**(반복 재생 목적이 아닌 경우에는 **MP3**)를 사용하세요.
- 자주 사용하는 짧은 소리(예: 발자국 소리, 총소리)에 **ADPCM**을 사용하세요. 이렇게 하면 압축되지 않은 PCM에 비해 파일이 줄지만 재생 중 디코딩은 빨라집니다.

모바일 기기에서의 음향 효과는 최대 22,050Hz여야 합니다. 낮은 설정을 사용해도 최종 품질에 미치는 영향은 일반적으로 매우 적으므로 직접 듣고 판단하세요.

적절한 로드 유형 선택

클립 크기에 따라 설정이 달라집니다.

- **작은 클립(< 200kb)**은 **로드 시 압축 해제**되어야 합니다. 이는 사운드를 가공되지 않은 16비트 PCM 오디오 데이터로 압축 해제하여 CPU 비용과 메모리 사용을 발생시키므로 짧은 사운드에만 적합합니다.
- **중간 클립(>= 200kb)**은 **메모리에서 압축**된 상태여야 합니다.
- **대용량 파일(배경 음악)** 은 **스트리밍**으로 설정해야 합니다. 그렇지 않으면 전체 에셋이 메모리에 한 번에 로드됩니다.

메모리에서 음소거된 AudioSource 언로드

음소거 버튼을 구현할 때 볼륨을 0으로 설정하지 마세요. 플레이어가 해당 기능을 자주 켜거나 끌 필요가 없다면 **AudioSource** 컴포넌트를 **삭제**하여 메모리에서 언로드할 수 있습니다.

전체 모바일 성능 팁 다운로드

다음 블로그 포스팅에서는 그래픽과 에셋에 대해 자세히 알아보겠습니다. 팀에서 제공하는 유용한 팁 목록을 모두 보고 싶다면 [여기](https://create.unity3d.com/optimize-mobile-game-eBook)에서 전자책을 다운로드하시기 바랍니다.

![Image of the ebook cover with red background and a graphic of an adventure game with a dragon and the words "Optimize your mobile game performance" in bold white text.](https://unity.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Ffuvbjjlp%2Fproduction%2F225107bd388b9cc42dc68ba30a7445c1027f1f6b-1133x1458.png&w=3840&q=75)

[전자책 다운로드](https://create.unity3d.com/optimize-mobile-game-eBook)

통합 지원 서비스에 대해 자세히 알아보고 엔지니어, 전문가 조언 및 프로젝트에 맞는 베스트 프랙티스 가이드를 이용하려면 [여기](https://unity.com/kr/success-plans)에서 유니티의 성공 플랜을 확인해 보세요.

더 많은 성능 팁 제공 예정

유니티는 Unity 애플리케이션이 최상의 성능을 발휘할 수 있도록 지원하기 위해 최선을 다하고 있습니다. 자세히 알고 싶은 최적화 주제가 있다면 댓글을 통해 알려 주시기 바랍니다.