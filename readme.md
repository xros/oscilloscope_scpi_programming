# Oscilloscope SCPI Programming using Python

By Songhua Liu

## Hardware

### Oscilloscope

My Oscilloscope is Rigol DHO924S (12bit, 250MHz, 1.25GSa/s, 50Mpts) which has AFG (Arbitrary Function Generator) and LA (Logic Analyser) built-in.

Docs can be found from [here](static/DHO900_pdf_files_en/) or its [website](https://www.rigol.com/).

#### Properties of the Oscilloscope

|Property| Specs | Notice|
|----|-------|-----------|
|ADC accuracy| 12 bit| 4096 (2^12) stairs vertically|
|Max Bandwidth| 250MHz | ADC chip onboard can meature freq upto 800MHz theoretically. When enabling FFT, it can meature low freq <= 625MHz with a proper probe.|
|Sampling Rate| 1.25GSa/s | Shared by 4 ADC channels. With only 1CH, it can reach 1.25GSa/s |
|Storage Depth| 50Mpts | Shared by 4 ADC channels.|
|AUX out| 1 port | Used for output triggerings and etc.|
|AFG out| 1 port | Arbitrary Function Generator |
|Ethernet LAN | Max at 1000Mbps full-duplex | Connected to router, screen sharing remotely using webview, and operating SCPI commands remotely via Ethernet |
|HDMI output | Max at 1920*1080 at 60FPS |Mirroring the screen only|
|USB 2.0 from back| 1 port | Connected to PC as a client for using SCPI commands and updating firmware|
|USB 2.0 from front| 1 port | USB host port for extra USB Wi-Fi dongle or USB disks on Android System.|
|Power| 1 USB-C | Can be powered using power bank at 12V or more |
|OS | Android 7.1.2 ||
|Firmware | 00.01.02.00.02 ||
|System Version | 1.2.2 ||

##### Front side

![front](static/image/71emYPnH+pL._AC_UF1000,1000_QL80_.jpg)

##### Back side

![back](static/image/DHO900-Back.jpg)

#### Properties of the Oscilloscope Probe

4 Probes come with the Rigol DHO924S.

|Property| Specs | Notice|
|----|-------|-----------|
|Name|PVP2350| |
|Max Freq| 350MHz| |
|Switch 1X | 1M ohm |For meaturing Voltage within 100V|
|Switch 10X | 10M ohm |For meaturing Voltage within 300V, also for calibrating probes initially|

#### Properties of the Oscilloscope AFG

|Property| Specs | Notice|
|----|-------|-----------|
|Sine Wave| max at 25MHz at 5V | The voltage can be higher with lower freq |
|Square Wave | max at 15MHz at 5V| Same as above |
|Other Waves | | Just read its doc|

#### Properties of the Oscilloscope LA

|Property| Specs | Notice|
|----|-------|-----------|
|Digital Channels| 16 ||
|Extra LA Probes | PLA 2216 | Optional. Needed to buy seperately or D.I.Y. one|
