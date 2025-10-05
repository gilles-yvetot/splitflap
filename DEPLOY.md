# How to update the code on the Splitflap ESP32

Open `code arduino/splitflap` inside VSCode. Not the root folder.

You'll need the VSCode extension "PlatformIO IDE" installed.

IT WILL NOT WORK ON CURSOR. They don't have the extension available. Someone built one but it does not work well.

[Useful links](https://github.com/scottbez1/splitflap/blob/master/docs/ElectronicsGuide.md)

## Before building

1. You will need to change the `SPLITFLAP_API_KEY` in `esp32/splitflap/http_task.cpp` to match your TOKEN from the splitflap client `app/api/users/_authenticate.ts`

1. You will need to copy the secrets file from `esp32/tester/secrets.h.example` to `esp32/splitflap/secrets.h` and fill in your WiFi credentials.

## Build

In the platformio tab,

Project Tasks > Default > General > Build all

It should print something like that:

```
============================================ [SUCCESS] Took 7.24 seconds ============================================

Environment         Status    Duration
------------------  --------  ------------
uno-shift-register  SUCCESS   00:00:07.239
============================================ 1 succeeded in 00:00:07.239 ============================================
```

If it builds successfully, you can upload it.

## Upload

Plug the cable to your computer and the ESP32.

Then Project Tasks > Default > General > Upload all
