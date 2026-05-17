# Dark Light Survivor RUS

![logo](logo.png)

---

## Как установить

Скачать файл согласно версии игры:

> 📦 **[Скачать релиз](https://github.com/AndyClashbit/Dark-Light-Survivor-RUS/releases/tag/VER_A_1.1.05172020)**
>
> *(если будут новые релизы — я буду указывать версию игры)*

Версию игры можно посмотреть на главном экране игры:

![версия игры](https://github.com/user-attachments/assets/679f21c8-7766-4544-a845-565cc4adb264)

Закинуть в `ВАШ_ДИСК:\SteamLibrary\steamapps\common\Dark Light Survivor\DLS\DLS_Data`, запустить игру — и локализация уже будет доступна.

Пример:

![пример](https://github.com/user-attachments/assets/ce912718-d0a4-4809-8609-d494224e287c)

---

## Используемые инструменты

### UABEA

UABEA — это инструмент для редактирования файлов ресурсов Unity (Asset Bundles и Serialized Files). Автор позиционирует его как инструмент для моддинга и исследований, а не для простого извлечения ресурсов.

| Назначение | Ссылка |
|---|---|
| Скачивание (релиз) | https://github.com/nesrak1/UABEA/releases |
| Скачивание (nightly) | https://github.com/nesrak1/UABEA |
| Для извлечения (альтернатива) | AssetRipper, AssetStudio |
| AddressablesTools | https://github.com/nesrak1/AddressablesTools |

**Назначение:** Предназначен для изменения данных внутри игры (текстуры, звуки, текст и т.д.).

---

### Как использовать UABEA

1. Скачайте и распакуйте UABEA
2. Запустите `UABEAvalonia.exe`
3. Нажмите сочетание клавиш `Ctrl+O` — откроется окно выбора файла

![ctrl+o](https://github.com/user-attachments/assets/00916bea-06e2-4389-8b00-f5ba16f5768e)

4. Выберите файл `resources.assets` из папки с игрой

![resources](https://github.com/user-attachments/assets/e8e8f3cb-438d-404b-a969-8eb5f75c92f6)

**Где найти resources.assets:**

- В Steam: `Библиотека → Dark Light Survivor → ПКМ → Свойства → Установленные файлы → Обзор`
- Путь: `.../steamapps/common/Dark Light Survivor/DLS/DLS_Data/resources.assets`

![путь](https://github.com/user-attachments/assets/5908dedf-428b-404d-9129-e4505aa1c8c3)

---

### Фильтрация файлов

После открытия файла нажмите `Ctrl+E` — откроется окно с фильтром:

![фильтр](https://github.com/user-attachments/assets/85abec15-3aac-42b9-85d1-2b9860d7c2cb)

- Нажмите **Deselect all**
- Поставьте галку на **MonoBehaviour**
- Закройте окно на крестик

![mono](https://github.com/user-attachments/assets/5e1e3530-bdac-4307-957c-e2223dfea652)

Теперь вы увидите все файлы с текстом и меню локализации.

---

### Основные файлы для перевода

**Path ID** — ищите в колонке справа:

| Path ID | Файл | Описание |
|---|---|---|
| **5652** | English (en-US) | Перевод меню. Если нужно — редактируйте, но не сломайте структуру JSON. Я использовал VS Code — он обычно подсвечивает, если что-то не так. |
| **5712** | Item Language Data EN | Какие-то айтемы, но я их не встретил в игре, потому что не особо играл, пока ковырялся. Найдете — поймете. Если что — скажите. |
| **5358** | MapInfoConfig | То, что вы видите на карте, когда выбираете локу для высадки. Там особо нечего переводить. |

---

### Как вытащить файл для редактирования

Это все отлично, но вы же сейчас спросите: «А как вытащить?» Да? Ща расскажу.

Для начала выберите файл, например пускай это будет English (en-US). Нажмите на него, и справа будет меню. Там кнопка **Export Dump** — жмете ее, и открывается окно с возможностью сохранить файл. Перед тем как сохранить, выберите тип файла **JSON**, потому что по умолчанию стоит TXT, и сохраните куда вам удобно.

После этого можно редактировать где вам удобно. Я же это делал в VS Code, как и говорил выше.

---

### Как вернуть файл обратно в игру

После того как отредактировали, есть два пути, как вернуть это обратно.

#### Вариант 1 — Edit Data

1. Выберите тот файл, который редактировали, в программе
2. Нажмите кнопку **Edit Data**

![edit_data_1](https://github.com/user-attachments/assets/1e8a84d0-cd73-4ea5-8c14-82d925ab90e3)
![edit_data_2](https://github.com/user-attachments/assets/c3de60d5-13fb-4413-a462-c4e9d6c376bf)

3. Скопируйте и вставьте то, что вы перевели, напрямую в редактор
4. Если горит красным — значит, вы что-то сломали в структуре JSON, переделывайте
5. Если же все **good**, нажмите сочетание клавиш `Ctrl+S` — все сохранится

![save](https://github.com/user-attachments/assets/a45ec570-a7f2-4e42-9893-b29e7b434b70)

6. Запускайте игру

---

#### Вариант 2 — Import Dump

1. Выберите тот файл, который редактировали, в программе
2. Нажмите **Import Dump**

![import_1](https://github.com/user-attachments/assets/3c994785-c6b2-4d31-8e1e-186ea0a97537)

3. Выберите тип файла **JSON**

![import_2](https://github.com/user-attachments/assets/bab7d2da-847d-4b5a-b9e9-12a055de45be)

4. Найдите то, что вы редактировали, и нажмите «Открыть» (или просто два раза кликните по файлу)

![import_3](https://github.com/user-attachments/assets/81a42735-dbb9-4e2c-be62-fcec3ea5ff25)

5. Файл добавится
6. Нажмите `Ctrl+S` — и все будет работать

![import_4](https://github.com/user-attachments/assets/59e819fd-3c06-42d9-9608-72d4f6eb6576)

7. Запускайте игру

---

### Как сохранить этот репозиторий себе

#### Способ 1: Через Git

1. Установите Git, если он у вас еще не установлен:
   - [Git for Windows](https://git-scm.com/download/win)

2. Откройте папку, куда хотите скачать файлы

3. Нажмите ПКМ по пустому месту в папке → «Открыть в Terminal» / «Open in Terminal»

4. Вставьте команду:

```bash
git clone https://github.com/AndyClashbit/Dark-Light-Survivor-RUS.git
```

5. Нажмите Enter и дождитесь окончания загрузки

6. После этого рядом появится папка `Dark-Light-Survivor-RUS` с переведенными JSON-файлами и остальными материалами

---

#### Способ 2: Без Git (просто скачать ZIP)

1. Зайдите на GitHub
2. Нажмите зеленую кнопку `Code`
3. Выберите `Download ZIP`
4. Распаковать архив в любое место