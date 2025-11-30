# flowsort-balanced-wave (Сортировка треков Spotify)

DJ-friendly tempo & key сортировка for Goofy / Spotify.

Этот скрипт реализует FlowSort.sortBalancedWave — сортировку треков с учётом темпа, тональностей (Camelot)
и базовых DJ-сценариев плавного развития в режиме (USE_KEY_SCENARIOS = true). Подходит для больших плейлистов (до 4000 треков) и
используется в экосистеме Goofy / Google Apps Script для работы со Spotify.

В режиме USE_KEY_SCENARIOS = false используется классическая гармоническая сортировка по Camelot с приоритетом темпа и без сценарных цепочек. Переключение режимов выполняется простым изменением значения флага USE_KEY_SCENARIOS вверху в коде (true ↔️ false).

Для работы скрипта требуется настроенный Goofy https://chimildic.github.io/goofy/#/ (к слову огромная благодарность автору проекта Goofy, без него ничего этого не было бы)

flowsort_sortBalancedWave.js нужно сохранить в отдельный файл и передвинуть повыше, к library.gs .

Вызывать функцию в скриптах нужно непосредственно перед формированием финального плейлиста (по принципу переменная  "tracks = FlowSort.sortBalancedWave(tracks);" . 
