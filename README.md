# SandTogether — фикс под Sandustry 0.6.0

Неофициальный фикс для мода [SandTogether](https://github.com/IronBamBam1990/sandtogether)
(автор — Kamil Padula, лицензия MIT; [мастерская Steam](https://steamcommunity.com/sharedfiles/filedetails/?id=3784750764)).

Мод 0.9.287-beta поддерживает Sandustry только до 0.5.7. После обновления игры до **0.6.0**
в код игры вставлялось всего ~5 из 42 хуков мода. Поэтому в коопе ломалось копание, установка
построек, пылесос, спрей, снаряды, существа, трубы и т.д.: у одного из игроков они не работали
или не синхронизировались.

Этот `patches.json` — оригинальный файл мода, в котором к каждому из 42 хуков добавлен вариант
под сборку 0.6.0. Варианты для старых версий игры оставлены без изменений.

## Установка (обоим игрокам, игра закрыта)

1. Скачайте [`patches.json`](patches.json) (кнопка Download raw file).
2. Замените им файл `src/patches.json` в папке мода `3784750764`:
   - **Windows:** `<библиотека Steam>\steamapps\workshop\content¾446084750764\src\`
   - **macOS:** `~/Library/Application Support/Steam/steamapps/workshop/content/2764460/3784750764/src/`
     (в Finder: Cmd+Shift+G и вставить путь)
3. Запустите установщик из папки `3784750764`:
   - **Windows:** `install.bat`
   - **macOS:** двойной клик по `install.command`
   В выводе должно быть 42 строки `[+] bundle.js: ...` и ни одной строки `[!] skipped`.
4. Запустите игру (на macOS — через `SandTogether-Launch.command`).

## Если что-то сломалось — лог

- **Windows:** `%APPDATA%\Sandustry\logs\main.log`
- **macOS:** `~/Library/Application Support/Sandustry/logs/main.log`

Если Steam обновит мод или игру, фикс может слететь — повторите шаги 2–3.
Если в мастерской выйдет версия мода с поддержкой 0.6.0, этот фикс больше не нужен.
