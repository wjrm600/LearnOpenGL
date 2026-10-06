# LearnOpenGL_Project

[LearnOpenGL](https://learnopengl.com/) 튜토리얼을 따라 공부하는 프로젝트입니다.

## 폴더 구조

```
LearnOpenGL_Project/
├── LearnOpenGL_Project.slnx        # Visual Studio 솔루션
├── LearnOpenGL_Project/            # 프로젝트
│   ├── LearnOpenGL_Project.vcxproj
│   └── src/                        # 소스 코드 (Main.cpp ...)
└── Dependencies/                   # 외부 라이브러리 (저장소에 포함)
    ├── glad/                       # OpenGL 3.3 Core 로더
    │   ├── include/  (glad/glad.h, KHR/khrplatform.h)
    │   └── src/glad.c
    └── glfw/                       # GLFW 3.5.1 (정적 라이브러리, MSVC x64)
        ├── include/GLFW/
        └── lib/Debug, lib/Release  (glfw3.lib)
```

모든 경로는 `$(ProjectDir)..\Dependencies\...` 형태의 상대 경로로 설정되어 있어서,
저장소를 clone 하면 추가 설치 없이 바로 빌드됩니다.

## 빌드 방법

1. Visual Studio 2026 (v145 툴셋, "C++를 사용한 데스크톱 개발" 워크로드)으로 `LearnOpenGL_Project.slnx` 열기
2. 구성: `Debug | x64` 또는 `Release | x64` 선택
3. 빌드 후 실행 (F5)

> GLFW 라이브러리는 x64 용으로만 포함되어 있으므로 x86(Win32) 구성은 링크되지 않습니다.
