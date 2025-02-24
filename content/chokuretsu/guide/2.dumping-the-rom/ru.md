---
title: 'ROM Дампинг'
navigation:
  current: '/dumping-the-rom'
  previous: '/buying-the-game'
  next: '/patching-the-rom'
---

Чтобы создать дамп ROM файла , помимо игры вам понадобится консоль Nintendo DS или 3DS. Для некоторых методов потребуются дополнительные устройства, такие как SD-карта или телефон, способный создать незащищённую точку доступа.

---

**Выберите платформу для дампа ROM файла:**
::guide-platform-filter
---
filters: ['Nintendo DS', 'Nintendo DSi', 'Nintendo 3DS']
---
<div class="platform-filtered platform-nintendo_ds">

### Дампинг на Nintendo DS или DS lite
Существует два способа дампа игры с помощью Nintendo DS или Nintendo DS lite. Оба требуют использования флеш-картриджа в первом слоте (гнездо для картриджа DS).

Первый метод использует взлом через Wi-Fi для дампа по протоколу передачи файлов (FTP). Второй метод потребует пару флэш-карт в 1 и 2 слоте (слот для картриджа GBA) для прямого ROM дампа .

#### Дамп через WI-Fii
**Требования:**
* Консоль Nintendo DS или DS lite.
* *Последовательности Харухи Судзумии*
* Флэш-картридж в первом слоте (например, картридж R4. Также карта SD или microSD для загрузки на нее данных по мере необходимости)
* Смартфон, планшет или другое устройство, которое может создавать незащищенную или защищенную WEP точку доступа Wi-Fi.
  - К сожалению, большинство современных компьютеров не способны на это. Лучшими устройствами для этого являются Android-смартфоны.
  - Устройства Apple и Windows (включая iPhone) не способны создавать незащищенные или защищенные с помощью WEP точки доступа.
* Компьютер, который вы можете использовать для [загрузки wooddumper] (https://digiex.net/threads/wood-dumper-dump-nintendo-ds-roms-and-save-games-over-wi-fi-with-an-nintendo-ds.14729/) и подключения к указанной точке доступа
* Игра DS с поддержкой Wi-Fi. Неважно, что поддержка закончилась. К сожалению, *Suzumiya Haruhi no Chokuretsu* не поддерживает Wi-Fi.

**Метод:**
1. С помощью смартфона, планшета или другого устройства, способного создать беспроводную точку доступа, создайте незащищенную (без пароля) или защищенную WEP точку доступа (должна быть защищена WEP, поскольку WPA и другие современные стандарты шифрования не поддерживаются DS).
2. На другом компьютере [загрузите wooddumper](https://digiex.net/threads/wood-dumper-dump-nintendo-ds-roms-and-save-games-over-wi-fi-with-an-nintendo-ds.14729/). Затем подключите этот компьютер к только что созданной точке доступа.
3. Установите wooddumper.nds (не версию для слота 2) в правую часть флэш-картриджа через SD-карту.
4. Вставьте игру Nintendo DS с поддержкой подключения Nintendo Wi-Fi и перейдите в меню Wi-Fi. Подключитесь к созданной вами точке доступа.
5. Выходим из игры и вынимаем картридж. Теперь вставьте флэш-картридж, на который вы только что установили Wooddumper, и запустите его на своем DS.
6. Следуйте инструкциям на экране и вставьте картридж с *Последовательностями Харухи Судзумии*, когда появится соответствующий запрос. Продолжайте, пока вам не будет предоставлен IP-адрес для подключения с помощью FTP-клиента.
7. Используя FTP-клиент, например [net2ftp](https://www.net2ftp.com/), встроенный браузер тот или иной, например [FileZilla](https://filezilla-project.org/), введите IP-адрес в соответствующее поле. Вам не нужно указывать имя пользователя или пароль.
8. Скопируйте .nds ROM и .txt файлына свой компьютер. Вы можете приступить к [Rom патчингу](/chokuretsu/guide/patching-the-rom).

#### Dump using dual-slot flash cartridges
**Requirements:**
* Nintendo DS or DS lite console
* *Suzumiya Haruhi no Chokuretsu*
* Slot-1 (DS slot) Flash cartridge (e.g. R4 cartridge)
* Slot-2 (GBA slot) Flash cartridge that is compatible with your Slot-1 cart (e.g. E-Link card)
* SD or microSD cards (or correct connection cables) to load and remove stuff from your flash cartridges, if necessary
* A computer you can use to download wooddumper

**Method:**
1. [Download wooddumper](https://digiex.net/threads/wood-dumper-dump-nintendo-ds-roms-and-save-games-over-wi-fi-with-an-nintendo-ds.14729/) on your computer.
2. Install the wooddumper_slot2.nds homebrew app onto the right part of your Slot-1 flash cart via the SD card.
3. Insert your Slot-1 and Slot-2 flash carts into your DS.
4. Open wooddumper via your flash cart.
5. Follow the on-screen instructions and insert your *Suzumiya Haruhi no Chokuretsu* cart when prompted. Proceed until you see that the dump has completed.
6. Remove your Slot-2 cart and insert the SD card from it into your PC (or in the case of some carts, connect it directly to your PC)
7. Copy the .nds ROM file and .txt file to your computer. You can proceed to [patching your ROM](/chokuretsu/guide/patching-the-rom).

</div>

<div class="platform-filtered platform-nintendo_dsi">

### Dumping with a Nintendo DSi

To dump using a Nintendo DSi, we will need to install a Custom Firmware (CFW) onto the system known as Twilight Menu++ and Unlaunch to let us run Godmode9i, which lets us dump the cartridge to an `.nds` file.

**Requirements:**
* Nintendo DSi or Nintendo DSi XL console
* *Suzumiya Haruhi no Chokuretsu*
* SD card with at least 2GB capacity
* Computer with an SD card reader/USB SD card reader peripheral

**Method:**
::guide-notice
Please take caution following these steps to avoid bricking your system.
::
1. Follow [the steps on dsi.cfw.guide](https://dsi.cfw.guide/launching-the-exploit.html) to install Twilight Menu++ and Unlaunch onto your DSi.
2. [Download GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) and extract the file using a utility such as 7Zip on Windows or The UnArchiver on macOS.
3. Remove the SD card from your DSi and insert it into your computer.
4. Place the extracted GodMode9.nds file anywhere on your SD card.
5. Insert the SD card back into your DSi.
6. Insert the *Suzumiya Haruhi no Chokuretsu* game cartridge into your DSi.
7. Launch Twilight Menu++ as you were shown and run GodMode9i.
8. Select the "NDS GAMECARD" option.
9. Press the A Button to select "yes" to dump your cartridge.
10. When complete, you can turn off your DSi and remove the SD card from the system.
11. Insert the SD card back into your computer. Navigate to (SD_CARD_ROOT)/gm9i/out/ on your SD card. Copy the .nds file to your computer.


</div>

<div class="platform-filtered platform-nintendo_3ds">

### Dumping with a Nintendo 3DS

To dump using a Nintendo 3DS or 2DS console, we will need to install a Custom Firmware (CFW) onto the system known as Luma3DS and bootstrap9 to let us run Godmode9, which lets us dump the cartridge to an .nds file.

**Requirements:**
* Nintendo 3DS, 3DS XL, 2DS, New 3DS, New 3DS XL or New 2DS XL console
* *Suzumiya Haruhi no Chokuretsu*
* SD card with at least 2GB capacity
* Computer with SD card reader/USB SD card reader peripheral
  * In some cases, you may need to use a DS or DSi-compatible flash cartridge.

**Method:**
::guide-notice
Please take caution following these steps to avoid bricking your system.
::
* Follow [the steps on 3ds.hacks.guide](https://3ds.hacks.guide/get-started) to install Luma3DS and bootstrap9 onto your 3DS.
* Continue following [the guide to install GodMode9](https://3ds.hacks.guide/finalizing-setup) as well as other prerequisite homebrew software onto your 3DS.
* Power off your console (not just sleep mode, a full power-off)
* Insert the *Suzumiya Haruhi no Chokuretsu* game cartridge into your 3DS.
* Hold the START button and press the Power Button to power on the console. This should launch GodMode9. If it doesn't, power off and try again.
* Use the D-Pad to navigate to `[C:] GAMECART`
* Press the A Button on `[TitleID].nds` to select it. If prompted to choose a dump type, press the A Button again.
* Select Copy to 0:/gm9/out on the lower screen to copy the dump to the SD card.
* When the dump has completed, power off your system and remove the SD card.
* Insert the SD card back into your computer. Navigate to /gm9/out/ on your SD card. Copy the .nds file to your computer.

</div>
::

---

## Before you proceed
You should now have dumped your game to a `.nds` ROM file that you can patch. Move this to somewhere easily accessible.

*ROM dumping information courtesy of [dumping.guide](https://dumping.guide/carts/nintendo/ds), [dsi.cfw.guide](https://dsi.cfw.guide/) & [3ds.hacks.guide](https://3ds.hacks.guide/) contributors.*