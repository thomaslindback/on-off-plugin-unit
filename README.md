# Multiple On Off plugin unit

Build on Windows

Setup esp-idf v5.2.3 as in:
https://docs.espressif.com/projects/esp-matter/en/latest/esp32/developing.html#esp-matter-setup

Run: .\install.ps1 esp32
And then .\export.ps1

Add esp-matter as dependency:
idf.py add-dependency "espressif/esp_matter^1.4.0"

Change paths in CMakeLists.txt (x2) to point back to esp-matter-main/examples/common/app_reset
and esp-matter-main/examples/common/utils

Commission as in:
https://docs.espressif.com/projects/esp-matter/en/latest/esp32/developing.html#commissioning

Matter shell is enabled.
Check the onboarding code: matter onboardingcodes none


python.exe .\components\esptool_py\esptool\esptool.py erase_region 0xC000 0x1000

