# PC Monitor

**[Русский](#русский) · [English](#english)**

---

## Русский

Бесплатная программа для геймеров на Windows: **FSR и генерация кадров в любой игре**, FPS с 1% low, подсказка, что тормозит, диагностика компьютера за неделю и мониторинг железа — в одном файле, на русском, без рекламы.

### Скачать

Раздел **Releases**, один файл — больше ничего ставить и скачивать не нужно:

| Система | Файл |
|---|---|
| Windows 10 / 11 (64-бит) | `PcMonitor-1.4.0.exe` |
| Windows 7 / 8 / 8.1 | больше не поддерживаются — последняя версия: [1.2.6](https://github.com/Ryydflw/pc-monitor/releases/tag/v1.2.6) |

При первом запуске Windows может показать «Windows защитила ваш компьютер» — так бывает со всеми новыми программами без платной цифровой подписи. Нажмите **Подробнее → Выполнить в любом случае**.

### Главное в 1.4

- **FSR в любой игре** — даже если в самой игре его нет. Игра рисует картинку меньшего размера, а PC Monitor увеличивает её до размера экрана по алгоритму **AMD FSR 1**: обычно **+30–50% FPS** почти без потери чёткости. Включается кнопкой или **Ctrl+Shift+F** прямо в игре. Режимы «Ультра качество», «Качество», «Баланс», «Производительность» и ползунок резкости.
- **Генерация кадров (бета)** — бесплатно, для отдельной видеокарты (NVIDIA GeForce, AMD Radeon RX); встроенная графика процессора (Intel UHD / Iris) её вместе с игрой не тянет — для неё лучше FSR с методом «PC Monitor». Промежуточные кадры дорисовываются до частоты монитора (например, 60 FPS игры → 144 на экране): картинка плавнее. Программа честно показывает, сколько кадров настоящих, а сколько сгенерировано.
- **Телефон как второй экран:** кнопка «Телефон» показывает QR-код, а на телефоне открываются FPS, температуры и нагрузка и кнопки управления: FSR, игровой режим, оверлей, тихий режим, очистка памяти, замер. Приложение не нужно.
- **Советчик:** упор в видеокарту — подскажет включить FSR; упор в процессор — подскажет, что FSR не поможет и что делать вместо него; FPS упирается в лимит — скажет, что ничего не нужно.
- **«Почему тормозит»:** если процессор сбрасывает частоту, программа скажет почему — перегрев, работа от батареи или лимит мощности.
- **Диагностика за неделю:** программа тихо собирает температуры, частоты и FPS, а через 7 дней показывает понятный отчёт — перегрев, высохшая термопаста (Hot Spot), износ SSD и батареи, нехватка памяти в играх. Есть **быстрая проверка** за 30 секунд и окно **«Все датчики»** с поиском.
- **Замер FPS (Ctrl+Shift+B):** минута игры — средний FPS, 1% и 0.1% low, минимум. История замеров и **картинка с результатом**, чтобы показать друзьям.
- **Проверка Windows:** найдёт фоновую запись Xbox, выключенный игровой режим Windows и план «Экономия энергии» — и исправит в один клик (с возвратом как было).
- **Новый дизайн:** тёмная тема, вкладки «Главная», «Игры», «Производительность», «Диагностика», круглые шкалы.
- **Тихий режим** для ноутбуков: без турбо-частоты — на 10–20 °C холоднее и тише.

### Всё остальное

- **FPS как в обзорах железа:** средний, минимальный, **1% low и 0.1% low**, микрофризы и **задержка вывода кадра** — в оверлее (**Ctrl+Shift+O**), статистике и на графиках.
- **Упор в процессор или видеокарту** — работает и на встроенной графике.
- **Игровой режим:** повышенный приоритет игре, план «Высокая производительность» (от сети), очистка памяти, пониженный приоритет фоновым программам. После игры всё возвращается.
- **Процессор, видеокарта, память, диски, сеть, вентиляторы, пинг, потребление** — графики в реальном времени.
- **Очистка памяти** как в Mem Reduct (**Ctrl+Shift+M**) и автоочистка.
- **Защита от перегрева**, **обновления** в один клик, **трей и мини-режим**, **запись в CSV**, окно **«О системе»** как в CPU-Z, **автозапуск**, русский и английский.

### Поддержать автора

Программа бесплатная и останется бесплатной. Если она вам помогла — поддержите разработку на **[Boosty](https://boosty.to/pcmonitor)** ❤

### Конфиденциальность

**Мы ничего о вас не собираем.** Нет аккаунтов, рекламы и телеметрии.
- Сайт для телефона включается только кнопкой «Телефон» и работает только в вашей домашней сети: случайный порт и секретный ключ из QR-кода, через интернет ничего не идёт.
- Датчики читаются у LibreHardwareMonitor на этом же компьютере (127.0.0.1).
- Пинг: раз в секунду на выбранный адрес уходит обычный ICMP-пакет без данных о вас. Можно выключить.
- Список поддержавших автора: при запуске скачивается файл `supporters.json` с GitHub (только имена для окна благодарностей).
- Обновления: при запуске и по кнопке программа спрашивает у GitHub номер последней версии.
- Диагностика за неделю и замеры FPS — только итоги, только на этом компьютере (`%LOCALAPPDATA%\PcMonitor`). Никуда не отправляются.
- FSR захватывает окно игры только для показа на экране: ничего не записывается и не сохраняется.
- Настройки хранятся только у вас в реестре (`HKCU\Software\PcMonitor`).

### Требования

Windows 10 версии 1903 или новее, или Windows 11 (64-бит); права администратора (нужны для датчиков, FPS и очистки памяти). Для FSR и генерации кадров — видеокарта с DirectX 11: подойдёт встроенная графика Intel начиная с процессоров Core 3-го поколения (2012) и любая дискретная AMD или NVIDIA.

### Ограничения

- **FSR и генерация кадров** работают с играми в окне или «без рамки». В эксклюзивном полноэкранном режиме картинку захватить нельзя. В Windows 10 вокруг игры видна тонкая жёлтая рамка захвата (в Windows 11 её нет).
- **FSR 1** — увеличение по одной картинке. Если в самой игре есть FSR 2/3 или DLSS — они лучше: им доступны данные движка.
- **Генерация кадров (бета)** добавляет задержку примерно на один кадр; на прицеле, тексте и при резких поворотах возможны искажения. Лучше всего — при 30–70 FPS игры.
- Встроенная графика Intel отдаёт меньше датчиков, чем дискретные AMD и NVIDIA.
- Без «умного» блока питания потребление системы — оценка.

### Отказ от ответственности

PC Monitor распространяется «как есть», без каких-либо гарантий. Автор не несёт ответственности за блокировки аккаунтов в играх, потерю игрового прогресса, сбои, перегрев или иной ущерб, связанный с использованием программы. Используйте на свой риск.

- **Программа не внедряется в игры** и не меняет их файлы и память. Оверлей и FSR — отдельные окна поверх игры: FSR берёт картинку стандартным захватом окна Windows (тем же, что используют программы для записи экрана), а FPS считается через PresentMon — стандартные события Windows (ETW). Поэтому риск срабатывания античита низкий, но гарантировать это для каждой игры невозможно. Если сомневаетесь — проверьте правила игры.
- **Программа не разгоняет железо** и не меняет напряжения и обороты вентиляторов — только показывает их.
- **Игровой режим, FSR и тихий режим** меняют приоритеты, план питания и размер окна игры только пока работают и возвращают всё после.

---

## English

A free tool for gamers on Windows: **FSR and frame generation in any game**, FPS with 1% low, a hint about what slows your game down, a weekly PC check-up and hardware monitoring — in a single file, no ads.

### Download

**Releases**, a single file — nothing else to install:

| System | File |
|---|---|
| Windows 10 / 11 (64-bit) | `PcMonitor-1.4.0.exe` |
| Windows 7 / 8 / 8.1 | no longer supported — last version: [1.2.6](https://github.com/Ryydflw/pc-monitor/releases/tag/v1.2.6) |

On first run Windows may show "Windows protected your PC" — this happens to every new program without a paid code-signing certificate. Click **More info → Run anyway**.

### What's new in 1.4

- **FSR in any game** — even one without FSR. The game renders a smaller picture and PC Monitor upscales it to the screen size with the **AMD FSR 1** algorithm: usually **+30–50% FPS** with almost no loss of sharpness. Turn it on with a button or **Ctrl+Shift+F** right in the game. Ultra quality, Quality, Balanced and Performance modes plus a sharpness slider.
- **Frame generation (beta)** — free, for a dedicated graphics card (NVIDIA GeForce, AMD Radeon RX); integrated processor graphics (Intel UHD / Iris) cannot run it together with the game — use FSR with the "PC Monitor" method instead. In-between frames are generated up to the monitor refresh rate (for example, 60 game FPS → 144 on screen) for smoother motion. The program honestly shows how many frames are real and how many are generated.
- **Advisor:** GPU-bound — suggests FSR; CPU-bound — explains that FSR won't help and what to do instead; capped FPS — says nothing is needed.
- **"Why is it slow":** if the CPU lowers its clock, the program tells you why — overheating, battery or a power limit.
- **Phone as a second screen:** the Phone button shows a QR code, and the phone opens FPS, temperatures and load plus controls: FSR, game mode, overlay, quiet mode, memory cleaning, benchmark. No app needed.
- **Weekly diagnostics:** the program quietly collects temperatures, clocks and FPS, and after 7 days shows a clear report — overheating, dried thermal paste (Hot Spot), SSD and battery wear, low memory in games. There is also a 30-second **quick check** and an **All sensors** window with search.
- **FPS benchmark (Ctrl+Shift+B):** one minute of gameplay — average FPS, 1% and 0.1% low, minimum. Benchmark history and a **result image** to share with friends.
- **Windows check:** finds Xbox background recording, disabled Windows Game Mode and the Power saver plan — and fixes them in one click (with undo).
- **New design:** dark theme, Home, Games, Performance and Diagnostics tabs, round gauges.
- **Quiet mode** for laptops: no turbo boost — 10–20 °C cooler and quieter.

### Everything else

- **FPS like in hardware reviews:** average, minimum, **1% low and 0.1% low**, stutters and **display latency** — in the overlay (**Ctrl+Shift+O**), statistics and charts.
- **CPU or GPU bottleneck** — works on integrated graphics too.
- **Game mode:** higher priority for the game, High performance power plan (on AC), RAM cleaning, lower priority for background programs. Everything is restored afterwards.
- **CPU, GPU, memory, disks, network, fans, ping, power** — real-time charts.
- **Memory cleaner** like Mem Reduct (**Ctrl+Shift+M**) and auto-clean.
- **Overheat protection**, one-click **updates**, **tray and mini mode**, **CSV recording**, **System info** like CPU-Z, **autostart**, Russian and English.

### Support the author

The program is free and will stay free. If it helped you, support development on **[Boosty](https://boosty.to/pcmonitor)** ❤

### Privacy

**We collect nothing about you.** No accounts, ads or telemetry.
- The phone page only turns on with the Phone button and only works on your home network: a random port and a secret key from the QR code, nothing goes over the internet.
- Sensors are read from LibreHardwareMonitor on the same computer (127.0.0.1).
- Ping: once a second a plain ICMP packet with no data about you goes to the chosen address. Can be turned off.
- Supporters list: at startup the file `supporters.json` is downloaded from GitHub (only names for the thank-you window).
- Updates: at startup and on the button the program asks GitHub for the latest version number.
- Weekly diagnostics and FPS benchmarks keep only totals, only on this computer (`%LOCALAPPDATA%\PcMonitor`). They are never sent anywhere.
- FSR captures the game window only to show it on screen: nothing is recorded or saved.
- Settings stay on your PC in the registry (`HKCU\Software\PcMonitor`).

### Requirements

Windows 10 version 1903 or newer, or Windows 11 (64-bit); administrator rights (for sensors, FPS and memory cleaning). FSR and frame generation need a DirectX 11 graphics card: Intel integrated graphics from 3rd-gen Core (2012) and any discrete AMD or NVIDIA card will do.

### Limitations

- **FSR and frame generation** work with games in windowed or borderless mode. The picture cannot be captured in exclusive fullscreen. On Windows 10 a thin yellow capture border is visible around the game (Windows 11 has none).
- **FSR 1** upscales a single image. If the game has its own FSR 2/3 or DLSS, they are better: they have access to engine data.
- **Frame generation (beta)** adds about one frame of latency; crosshairs, text and fast turns may show artifacts. Works best at 30–70 game FPS.
- Intel integrated graphics expose fewer sensors than discrete AMD and NVIDIA cards.
- Without a smart PSU, system power is an estimate.

### Disclaimer

PC Monitor is provided "as is", without any warranty. The author is not responsible for game account bans, lost game progress, crashes, overheating or any other damage related to using the program. Use at your own risk.

- **The program does not inject into games** and does not change their files or memory. The overlay and FSR are separate windows on top of the game: FSR takes the picture with the standard Windows window capture (the same one screen recorders use), and FPS is measured with PresentMon — standard Windows events (ETW). So the risk of triggering an anti-cheat is low, but it cannot be guaranteed for every game. If in doubt, check the game's rules.
- **The program does not overclock** and does not change voltages or fan speeds — it only shows them.
- **Game mode, FSR and quiet mode** change priorities, the power plan and the game window size only while they are on, and restore everything afterwards.

---

### Благодарности / Credits

- **AMD FidelityFX Super Resolution 1** (MIT) — алгоритм масштабирования / upscaling algorithm ([GPUOpen-Effects/FidelityFX-FSR](https://github.com/GPUOpen-Effects/FidelityFX-FSR)).
- **Mem Reduct** — автор **Henry++** ([github.com/henrypp/memreduct](https://github.com/henrypp/memreduct)). Очистка памяти в PC Monitor сделана по идее Mem Reduct; код Mem Reduct не используется — программа сама вызывает те же функции Windows. / The memory cleaner follows the idea of Mem Reduct by Henry++; no Mem Reduct code is used.
- **CPU-Z** — **CPUID** ([cpuid.com](https://www.cpuid.com/softwares/cpu-z.html)). Окно «О системе» сделано по идее CPU-Z; CPU-Z в программу не входит — сведения собираются своим кодом. / The System info window follows the idea of CPU-Z by CPUID; CPU-Z is not included.
- **LibreHardwareMonitor** (MPL 2.0) — датчики / sensors.
- **Intel PresentMon** (MIT) — FPS.
- **Qt** (LGPL v3) — интерфейс / UI.

See `THIRD-PARTY-NOTICES.txt` inside the program.
