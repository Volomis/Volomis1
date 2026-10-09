# EmptyWindowCpp

Минимальное нативное приложение Windows на C++: при запуске открывает пустое окно с иконкой круглых розовых линз в тонкой золотой оправе. Закрытие окна завершает приложение.

## Структура

- `src/main.cpp` — создание окна и цикл обработки сообщений Win32.
- `assets/app.ico` — иконка приложения, встроенная в EXE.
- `assets/pink-glasses.png` — исходное изображение иконки.
- `app.rc` и `resource.h` — подключение иконки как ресурса Windows.
- `CMakeLists.txt` — описание сборки проекта.
- `build/EmptyWindow.exe` — собранная программа (локальная сборка).

## Сборка через MinGW-w64

Из корня проекта выполните:

```powershell
windres app.rc -O coff -o build/app.res.o
g++ -std=c++17 -municode -mwindows -DUNICODE -D_UNICODE -I. src/main.cpp build/app.res.o -o build/EmptyWindow.exe
```

Для Windows x64. В проекте не используются сторонние библиотеки.
