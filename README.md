# Change Language on Sony A7R III (ILCE-7RM3)

## Unlock All Languages and Change Language on Sony A7R III (ILCE-7RM3)

---

## Requirements

- Sony A7R III camera with firmware version 3.10  
- Windows PC  
- Download pmca-console for Windows from the official releases page:  
  [https://github.com/ma1co/Sony-PMCA-RE/releases](https://github.com/ma1co/Sony-PMCA-RE/releases)   
- USB cable to connect the camera  
- [Zadig](https://zadig.akeo.ie/) (for installing libusb drivers, if needed)  

---

## Steps

### 1. Connect your camera to the PC in Mass Storage mode

- Turn on the camera and select **Mass Storage (USB Mode)**.

### 2. Launch pmca-console in service mode

Open PowerShell or Command Prompt, navigate to the pmca-console folder, and run:

```powershell
.\pmca-console-v0.18-22-ga82f5ba-win.exe serviceshell
```
Wait until you see the shell prompt:

```
Welcome to platform shell.
Type `help` for the list of supported commands.
Type `exit` to quit.
>
```
3. Unlock all languages via Tweak
At the prompt, type:

```
tweak
```
You will see a list of options like this:

```
1: [ ] Disable video recording limit
2: [ ] Unlock all languages
3: [X] Enable PAL / NTSC selector & warning
4: [X] Enable USB app installer
```

To enable unlocking all languages, type:

```
2
```
You should see a checkmark [X] appear next to Unlock all languages.

Then apply changes by typing:

```
0
```
Note: If you get an error Cannot overwrite backup, it means the setting is already enabled.

4. Exit the shell and reboot the camera
Type:

```
exit
```
Then reboot the camera with:

```
.\pmca-console-v0.18-22-ga82f5ba-win.exe reboot
```
5. Check the camera menu language
After reboot, open your camera menu and you should be able to select English or any other unlocked language.

## Notes

- **Driver installation:** Make sure to install the **libusb** drivers using [Zadig](https://zadig.akeo.ie/) if pmca-console does not detect your camera.
- **Firmware compatibility:** This method works on firmware **3.10 and later**.
- **Third-party apps:** No need to install third-party apps for this language unlock method.
- **Help commands:** Use the `help` command inside the service shell to explore additional options.
- **Error handling:** If you encounter `Cannot overwrite backup` error, it means the tweak is already enabled.

