# ESP-IDF in Visual Studio 2022

## Introduction:
This guide is based on the [post on ESP32 Forums](https://esp32.com/viewtopic.php?f=40&t=18924) with updated information.

## Prerequisites:
<ul>
  <li> Visual Studio Community 2022
    <ul>
      <li> Desktop Development with C++ </li>
      <li> Linux and embedded development with C++ </li>
    </ul>
</ul>

### Optional:
<ul>
  <li> Resharper C++
</ul>

## Instructions:

1. Download the ESP-IDF Tools installer [for Windows](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/windows-setup.html)
2. Run the installer. Warning: Do not install in to folder that contains spaces.
3. Create a new project by copying the hello_world example folder (`C:\Users\[username]\Desktop\esp-idf\examples\get-started\hello_world`) to the place you want (the full directory path should not contain any spaces).
4. Right click your project folder in Windows Explorer and select 'Open with Visual Studio' or you can just open Visual Studio 2022 from Start Menu.
5. Choose File - Open - CMake, and select your project folder. Wait until 'CMake Overview Pages' is shown.
6. Click 'Edit JSON'
7. Replace all with the code from `CMakeSettings.json` and change the `USERNAME`, `FLASH_COM_PORT` and some paths if needed. Warning: updating ESP-IDF breaks the compatibility because paths change. Save file.
8. Right click any file in the Solution Explorer and choose Configure Tasks. Replace all with code from `tasks_schema.json` and save file.
9. TODO


## Troubleshooting:

If Python doesn't work: Set `python` environment variable in the 'System Environment Variables' to `C:\Users\[username]\.espressif\python_env\idf4.4_py3.8_env\Scripts\python.exe`
