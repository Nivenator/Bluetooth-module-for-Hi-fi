# ESP32 Bluetooth Hi-Fi Receiver

A Bluetooth Hi-Fi receiver built around the ESP32 that streams high-quality audio directly to an existing Hi-Fi system. An OLED display provides track information such as title, artist and playback progress, creating an experience similar to a dedicated audio component.

*This device produces a line-level output and is not suitable to drive speakers, to do this consider switching the DAC to one that includes and amplifier.

## Why I made this

As someone who received there first their first HI-FI, I loved the physical media and high audio quality. However the price of CDs add up quickly and charity shops or Vinted are luck of the draw. On top of that sometimes I only like a few songs on an album so buying it seems excessive. This system allows me to simply stream the songs from services like Spotify or Youtube straight to the audio in port of my system. As an added benefit it also allows me to take advantage of my speakers for movie nights. 

## Features

- Bluetooth A2DP audio streaming
- High\-quality digital line-level audio output via I2S DAC
- OLED display showing: 
    - Song title
    - Artist name
    - Track duration
    - Playback progress bar
    - With extra information on names removed such as remaster date etc.
- Automatic scrolling for long song titles and artist names
- Real-time metadata updates using AVRCP
- Custom user interface designed for embedded hardware

## How It Works

The ESP32 uses an A2DP library to stream Bluetooth directly to the DAC using I2S communictaion

Track metadata is retrieved using AVRCP and displayed on the OLED screen. Information including the song title, artist name and track duration is automatically updated when a new track is detected. The titles are also shortened by removing "unnecessary" data like remaster date or video available.

For improved usability, song titles and artist names that exceed the display width automatically scroll across the screen. A progress bar provides a visual indication of playback position, whilst elapsed and total playback times are displayed at the bottom of the screen.

## Hardware Used

- ESP32 Development Board
    An ESP32 VROOM was used in my setup, however most ESP32 dev boards should work as long as they have Bluetooth capabilities and 3.3V, 5V and at least 5 available GPIO pins.
- SH1106 128×64 OLED Display
    A 1.3 inch screen chosen for compatibility with I2C and suitable size but could be switched with some code changes
- Adafruit PCM5102 I2S DAC
    Chosen for its high audio quality, line-level output and simple integration with the ESP32 via I²S. The PCM5102 does not require an external master clock, reducing wiring complexity and GPIO usage.
- 5V USBc power cable
- Jumper cables

## Software and Libraries

The project was developed using the Arduino IDE and utilizes the following libraries:

- AudioTools
- ESP32\-A2DP
- Adafruit GFX
- Adafruit SH110X
- Wire

## Project Images

### Hardware Setup

Photos will be inserted here later

### OLED Screen Example

<img width="450" height="300" alt="image" src="https://github.com/user-attachments/assets/9131c399-30c4-4790-96cd-b4368a2e7b04" />

### Internal Electronics

Photos will be inserted here later

## Future Improvements

Potential future developments include:

- Rotary encoder volume and menu control
- Better time bar that accounts for pausing/skipping ahead
- Integration with ESP32 NOW/Home
- Added features such as an alarm mode
- Wi\-Fi streaming support
- Equalizer functionality
- Multiple display themes

## Acknowledgements

This project uses the following open\-source libraries:

- AudioTools
- ESP32\-A2DP
- Adafruit GFX
- Adafruit SH110X

Display graphics and interface elements were designed using Lopaka.

## License

This project is licensed under the MIT License.

