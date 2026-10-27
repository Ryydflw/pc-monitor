# PC Monitor

**[Русский](#русский) · [English](#english)**

---

## Русский

Мониторинг ПК в реальном времени для Windows: графики CPU, GPU, ОЗУ, потребления, пинга и FPS игр, оверлей поверх игры, очистка памяти и защита от перегрева.

### Скачать

Раздел **Releases**, один файл — больше ничего ставить и скачивать не нужно:

| Система | Файл |
|---|---|
| Windows 10 / 11 (64-бит) | `PcMonitor-1.3.0.exe` |
| Windows 7 / 8 / 8.1 (64-бит) | `PcMonitor-1.3.0-win7.exe` |

При первом запуске Windows может показать «Windows защитила ваш компьютер» — так бывает со всеми новыми программами без платной цифровой подписи. Нажмите **Подробнее → Выполнить в любом случае**.

### Возможности

- **Экран загрузки:** видно, как запускаются датчики, счётчик FPS, пинг и очистка памяти.
- **Процессор:** загрузка, температура, частота (как в Диспетчере задач), мощность.
- **Видеокарта:** загрузка, температура, частота, мощность, видеопамять.
- **ОЗУ** и **очистка памяти** как в Mem Reduct: кнопка, **Ctrl+Shift+M** и автоочистка при заполнении на 90%. Во время игры память самой игры не трогается.
- **Пинг** с джиттером и потерями (адрес выбирается в настройках).
- **Потребление системы:** реальное, если у блока питания есть датчик (Corsair HXi/AXi/RMi, ASUS Thor), иначе — оценка с разбивкой CPU + GPU + прочее.
- **FPS как в обзорах железа:** средний, минимальный, **1% low и 0.1% low** — в оверлее, панели статистики и на графике. Микрофризы отмечаются красными точками. Игру можно выбрать вручную.
- **Упор в процессор или видеокарту:** программа показывает, что ограничивает FPS — видеокарта, процессор или лимит кадров (VSync), и что с этим сделать. Работает и на встроенной графике.
- **Игровой режим:** пока идёт игра — повышенный приоритет игре, план питания «Высокая производительность» (от сети), очистка памяти и пониженный приоритет фоновым браузерам и лаунчерам. После игры всё возвращается. Прирост обычно 0–10%, больше всего — на слабых ноутбуках.
- **Сводка сверху:** игра, FPS с 1% low, упор, температуры, память и потребление — крупными плитками.
- **Панель «Статистика»** у левого края и **оверлей** поверх игры (**Ctrl+Shift+O**).
- **Защита от перегрева:** при 80 °C и выше игра сворачивается (или закрывается — по выбору).
- **Обновления:** при запуске программа сама проверяет GitHub и предлагает «Обновиться / Не сейчас»; новая версия скачивается и ставится сама. В версии для Windows 7 файл скачивается через браузер.
- **Вентиляторы, диски и сеть:** обороты вентиляторов, температура SSD, скорость чтения/записи дисков, скорость загрузки и отдачи.
- **О системе** как в CPU-Z: модель процессора, ядра, кэши, инструкции, материнская плата, BIOS, модули памяти, видеокарта и драйвер.
- **Запись в CSV:** все показатели в таблицу, чтобы сравнить «до и после разгона».
- **Трей и мини-режим:** значок у часов с температурой или FPS, маленькое окно с четырьмя цифрами поверх всех окон.
- **Экономия энергии** для ноутбуков: от батареи программа обновляется реже; свёрнутая в трей почти не тратит процессор.
- **Тёмная и светлая темы**, выбор цвета акцента.
- **Автозапуск** с Windows, **языки** русский и английский.

### Поддержать автора

Программа бесплатная и останется бесплатной. Если она вам помогла — поддержите разработку на **[Boosty](https://boosty.to/pcmonitor)** ❤

### Конфиденциальность

**Мы ничего о вас не собираем.** Нет аккаунтов, рекламы и телеметрии.
- Датчики читаются у LibreHardwareMonitor на этом же компьютере (127.0.0.1).
- Пинг: раз в секунду на выбранный адрес уходит обычный ICMP-пакет без данных о вас. Можно выключить.
- Список поддержавших автора: при запуске скачивается файл `supporters.json` с GitHub (только имена для окна благодарностей).
- Обновления: при запуске и по кнопке программа спрашивает у GitHub номер последней версии. Если вышла новая — появится окно «Обновиться / Не сейчас».
- Настройки хранятся только у вас в реестре (`HKCU\Software\PcMonitor`).

### Требования

64-битная Windows, права администратора (нужны для датчиков, FPS и очистки памяти), .NET Framework 4.7.2+ (в Windows 10/11 уже есть; на Windows 7 SP1 ставится отдельно).

### Ограничения

- Встроенная графика Intel отдаёт только частоту; полные данные — на дискретных AMD и NVIDIA.
- Без «умного» блока питания потребление системы — оценка.
- В эксклюзивном полноэкранном режиме игра может перекрыть оверлей — используйте «оконный без рамки».
- Версия для Windows 7 не проверялась на настоящей Windows 7.

### Отказ от ответственности

PC Monitor распространяется «как есть», без каких-либо гарантий. Автор не несёт ответственности за блокировки аккаунтов в играх, потерю игрового прогресса, сбои, перегрев или иной ущерб, связанный с использованием программы. Используйте на свой риск.

- **Программа не внедряется в игры** и не меняет их файлы и память. Оверлей — отдельное окно поверх игры, а FPS считается через PresentMon — стандартные события Windows (ETW), которые использует и сама Windows. Поэтому риск срабатывания античита низкий, но гарантировать это для каждой игры невозможно. Если сомневаетесь — проверьте правила игры.
- **Программа не разгоняет железо** и не меняет напряжения и обороты вентиляторов — только показывает их.
- **Игровой режим** меняет приоритеты процессов и план питания только на время игры и возвращает всё после неё.

---

## English

Real-time PC monitoring for Windows: CPU, GPU, RAM, power, ping and game FPS charts, an in-game overlay, a memory cleaner and overheat protection.

### Download

**Releases**, a single file — nothing else to install:

| System | File |
|---|---|
| Windows 10 / 11 (64-bit) | `PcMonitor-1.3.0.exe` |
| Windows 7 / 8 / 8.1 (64-bit) | `PcMonitor-1.3.0-win7.exe` |

On first run Windows may show "Windows protected your PC" — this happens to every new program without a paid code-signing certificate. Click **More info → Run anyway**.

### Features

- **Loading screen** showing sensors, FPS counter, ping and memory cleaner starting up.
- **Processor:** load, temperature, clock (as in Task Manager), power.
- **Graphics card:** load, temperature, clock, power, video memory.
- **RAM** and a **memory cleaner** like Mem Reduct: button, **Ctrl+Shift+M** and auto-clean at 90% usage. During a game the game's own memory is left alone.
- **Ping** with jitter and packet loss (address set in Settings).
- **System power:** measured if your PSU has a sensor (Corsair HXi/AXi/RMi, ASUS Thor), otherwise an estimate with a CPU + GPU + other breakdown.
- **FPS like in hardware reviews:** average, minimum, **1% low and 0.1% low** — in the overlay, statistics panel and chart. Stutters are marked with red dots. The tracked game can be chosen manually.
- **CPU or GPU bottleneck:** the program shows what limits your FPS — the graphics card, the processor or a frame cap (VSync) — and what to do about it. Works on integrated graphics too.
- **Game mode:** while a game runs — higher priority for the game, High performance power plan (on AC), RAM cleaning and lower priority for background browsers and launchers. Everything is restored afterwards. The gain is usually 0–10%, most on weak laptops.
- **Summary on top:** game, FPS with 1% low, bottleneck, temperatures, memory and power as big tiles.
- **Statistics panel** on the left edge and an in-game **overlay** (**Ctrl+Shift+O**).
- **Overheat protection:** at 80 °C or more the game is minimized (or closed — your choice).
- **Updates:** at startup the program checks GitHub and offers "Update / Not now"; the new version downloads and installs itself. In the Windows 7 edition the file is downloaded via the browser.
- **Fans, disks and network:** fan speeds, SSD temperature, disk read/write speed, download and upload speed.
- **System info** like CPU-Z: CPU model, cores, caches, instruction sets, motherboard, BIOS, memory modules, graphics card and driver.
- **CSV recording:** all values to a table to compare "before and after overclocking".
- **Tray and mini mode:** a tray icon showing temperature or FPS, and a small always-on-top window with four numbers.
- **Power saving** for laptops: on battery the program refreshes less often; minimized to the tray it uses almost no CPU.
- **Dark and light themes**, accent colour choice.
- **Autostart** with Windows, **languages** Russian and English.

### Support the author

The program is free and will stay free. If it helped you, support development on **[Boosty](https://boosty.to/pcmonitor)** ❤

### Privacy

**We collect nothing about you.** No accounts, ads or telemetry.
- Sensors are read from LibreHardwareMonitor on the same computer (127.0.0.1).
- Ping: once a second a plain ICMP packet with no data about you goes to the chosen address. Can be turned off.
- Supporters list: at startup the file `supporters.json` is downloaded from GitHub (only names for the thank-you window).
- Updates: at startup and on the button the program asks GitHub for the latest version number. If a new one is out, you get an "Update / Not now" prompt.
- Settings stay on your PC in the registry (`HKCU\Software\PcMonitor`).

### Requirements

64-bit Windows, administrator rights (for sensors, FPS and memory cleaning), .NET Framework 4.7.2+ (built into Windows 10/11; install separately on Windows 7 SP1).

### Limitations

- Intel integrated graphics report only the clock; full data on discrete AMD and NVIDIA cards.
- Without a smart PSU, system power is an estimate.
- In exclusive fullscreen a game may cover the overlay — use borderless windowed mode.
- The Windows 7 edition has not been tested on a real Windows 7 machine.

### Disclaimer

PC Monitor is provided "as is", without any warranty. The author is not responsible for game account bans, lost game progress, crashes, overheating or any other damage related to using the program. Use at your own risk.

- **The program does not inject into games** and does not change their files or memory. The overlay is a separate window on top of the game, and FPS is measured with PresentMon — standard Windows events (ETW) that Windows itself uses. So the risk of triggering an anti-cheat is low, but it cannot be guaranteed for every game. If in doubt, check the game's rules.
- **The program does not overclock** and does not change voltages or fan speeds — it only shows them.
- **Game mode** changes process priorities and the power plan only while a game runs and restores everything afterwards.

---

### Благодарности / Credits

- **Mem Reduct** — автор **Henry++** ([github.com/henrypp/memreduct](https://github.com/henrypp/memreduct)). Очистка памяти в PC Monitor сделана по идее Mem Reduct; код Mem Reduct не используется — программа сама вызывает те же функции Windows. / The memory cleaner follows the idea of Mem Reduct by Henry++; no Mem Reduct code is used.
- **CPU-Z** — **CPUID** ([cpuid.com](https://www.cpuid.com/softwares/cpu-z.html)). Окно «О системе» сделано по идее CPU-Z; CPU-Z в программу не входит — сведения собираются своим кодом. / The System info window follows the idea of CPU-Z by CPUID; CPU-Z is not included.
- **LibreHardwareMonitor** (MPL 2.0) — датчики / sensors.
- **Intel PresentMon** (MIT) — FPS.
- **Qt** (LGPL v3) — интерфейс / UI.

See `THIRD-PARTY-NOTICES.txt` inside the program.
