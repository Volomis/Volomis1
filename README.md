# EmptyWindowCpp

Минимальное нативное приложение Windows на C++: при запуске открывает пустое окно. Закрытие окна завершает приложение.

## Структура

- `src/main.cpp` — создание окна и цикл обработки сообщений Win32.
- `CMakeLists.txt` — описание сборки проекта.
- `build/EmptyWindow.exe` — собранная программа (локальная сборка).

## Сборка через MinGW-w64

Из корня проекта выполните:

```powershell
g++ -std=c++17 -municode -mwindows -DUNICODE -D_UNICODE src/main.cpp -o build/EmptyWindow.exe
```

Для Windows x64. В проекте не используются сторонние библиотеки.
