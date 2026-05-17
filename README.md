# Dark Light Survivor RUS

![logo](logo.png)

## Как установить

Скачать файл согласно версии игры: https://github.com/AndyClashbit/Dark-Light-Survivor-RUS/releases/tag/VER_A_1.1.05172020 (если будут новые релизы то я буду указывать версию игры)

Версию игры можно посмотреть на главном экране игры:

![версия игры](https://github.com/user-attachments/assets/679f21c8-7766-4544-a845-565cc4adb264)

Закинуть в `ВАШ_ДИСК:\SteamLibrary\steamapps\common\Dark Light Survivor\DLS\DLS_Data`, запустить игру — и локализация уже будет доступна.
Пример ![пример](https://github.com/user-attachments/assets/ce912718-d0a4-4809-8609-d494224e287c)

---

## Используемые инструменты

### UABEA

UABEA — это инструмент для редактирования файлов ресурсов Unity (Asset Bundles и Serialized Files). Автор позиционирует его как инструмент для моддинга и исследований, а не для простого извлечения ресурсов.

**Скачивание:** Используйте последний релиз (https://github.com/nesrak1/UABEA/releases) или ночную сборку (Nightly) из раздела UABEANext (https://github.com/nesrak1/UABEA) (она более современная, с поддержкой вкладок).

**Назначение:** Предназначен для изменения данных внутри игры (текстуры, звуки, текст и т.д.).

**Для простого извлечения:** Автор рекомендует использовать AssetRipper (https://github.com/AssetRipper/AssetRipper) или AssetStudio (https://github.com/Perfare/AssetStudio/), если вам нужно просто вытащить файлы из игры.

**Addressables:** Если игра использует систему Addressables (пути типа StreamingAssets/aa/...), перед редактированием нужно снять CRC-проверки с помощью AddressablesTools (https://github.com/nesrak1/AddressablesTools).

### Как использовать UABEA

1. Скачайте и распакуйте UABEA.
2. Запустите `UABEAvalonia.exe`.
3. Нажмите сочетание клавиш `Ctrl+O` — откроется окно выбора файла.
![ctrl+o](https://github.com/user-attachments/assets/00916bea-06e2-4389-8b00-f5ba16f5768e)

4. Выберите файл `resources.assets` из папки с игрой.
![resources](https://github.com/user-attachments/assets/e8e8f3cb-438d-404b-a969-8eb5f75c92f6)

**Где найти resources.assets:**
- В Steam: Библиотека → Dark Light Survivor → ПКМ → Свойства → Установленные файлы → Обзор
- Путь: `.../steamapps/common/Dark Light Survivor/DLS/DLS_Data/resources.assets`
![путь](https://github.com/user-attachments/assets/5908dedf-428b-404d-9129-e4505aa1c8c3)

### Фильтрация файлов

После открытия файла нажмите `Ctrl+E` — откроется окно с фильтром:
![фильтр](https://github.com/user-attachments/assets/85abec15-3aac-42b9-85d1-2b9860d7c2cb)
- Нажмите **Deselect all**
- Поставьте галку на **MonoBehaviour**
- Закройте окно на крестик
![mono](https://github.com/user-attachments/assets/5e1e3530-bdac-4307-957c-e2223dfea652)

Теперь вы увидите все файлы с текстом и меню локализации.

### Основные файлы для перевода

- **5652 - English (en-US)** — перевод меню
- **5712 - Item Language Data EN** — какие-то айтемы (не встречались в игре)
- **5358 - MapInfoConfig** — названия карт при выборе локации

### Экспорт и импорт файлов

1. Выберите файл (например, English (en-US))
2. Справа будет меню с кнопкой **Export Dump**
3. Нажмите её — откроется окно сохранения
4. Выберите тип файла **JSON** (по умолчанию txt)
5. Сохраните файл
6. Редактируйте в любом текстовом редакторе (рекомендуется VS Code — он подсвечивает ошибки в JSON)

Для импорта используйте кнопку **Import Dump**.