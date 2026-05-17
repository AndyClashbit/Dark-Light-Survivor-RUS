# Dark Light Survivor RUS

![logo](logo.png)

## Как установить

Скачать файл согласно версии игры: https://github.com/AndyClashbit/Dark-Light-Survivor-RUS/releases/tag/VER_A_1.1.05172020 (если будут новые релизы то я буду указывать версию игры)

Версию игры можно посмотреть на главном экране игры:

![версия игры](https://github.com/user-attachments/assets/679f21c8-7766-4544-a845-565cc4adb264)

Закинуть в `ВАШ_ДИСК:\SteamLibrary\steamapps\common\Dark Light Survivor\DLS\DLS_Data`, запустить игру — и локализация уже будет доступна.

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
4. Выберите файл `resources.assets` из папки с игрой.

**Где найти resources.assets:**
- В Steam: Библиотека → Dark Light Survivor → ПКМ → Свойства → Установленные файлы → Обзор
- Путь: `.../steamapps/common/Dark Light Survivor/DLS/DLS_Data/resources.assets`

### Фильтрация файлов

После открытия файла нажмите `Ctrl+E` — откроется окно с фильтром:
- Нажмите **Deselect all**
- Поставьте галку на **MonoBehaviour**
- Закройте окно на крестик

Теперь вы увидите все файлы с текстом и меню локализации.