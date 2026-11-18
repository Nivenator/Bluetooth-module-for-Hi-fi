# ESP32 Bluetooth Hi\-Fi Receiver

A portable Bluetooth Hi\-Fi receiver built using an ESP32, external I2S DAC and SH1106 OLED display. The device streams audio from a phone, laptop or tablet via Bluetooth A2DP whilst displaying track metadata, playback progress and song timing information on a dedicated OLED interface.

## Features

- Bluetooth A2DP audio streaming
- High\-quality digital audio output via I2S DAC
- OLED display showing: 
    - Song title
    - Artist name
    - Track duration
    - Playback progress bar
- Automatic scrolling for long song titles and artist names
- Real\-time metadata updates using AVRCP
- Custom user interface designed for embedded hardware

## Hardware Used

- ESP32 Development Board
- SH1106 128×64 OLED Display
- Adafruit PCM5102 I2S DAC 
- 5V USBc power cable
- Connecting Wires

## Software and Libraries

The project was developed using the Arduino IDE and utilizes the following libraries:

- AudioTools
- ESP32\-A2DP
- Adafruit GFX
- Adafruit SH110X
- Wire

## How It Works

The ESP32 acts as a Bluetooth A2DP sink, allowing audio to be streamed from a Bluetooth source such as a smartphone. Audio data is transmitted digitally through an I2S interface to an external DAC for playback.

Track metadata is retrieved using AVRCP and displayed on the OLED screen. Information including the song title, artist name and track duration is automatically updated when a new track is detected. The titles are also shortened by removing "unnecessary" data like remaster date or video available.

For improved usability, song titles and artist names that exceed the display width automatically scroll across the screen. A progress bar provides a visual indication of playback position, whilst elapsed and total playback times are displayed at the bottom of the screen.

## User Interface

The OLED interface displays:

- Current song title
- Current artist
- Playback progress bar
- Elapsed time
- Total track duration

Long metadata fields automatically scroll to ensure all information remains visible.

## Project Images

### Hardware Setup

Photos will be inserted here later

### OLED Interface

Photos will be inserted here later

### Internal Electronics

Photos will be inserted here later

## Future Improvements

Potential future developments include:

- Rotary encoder volume control
- Added features such as an alarm mode
- Playback controls (play/pause, next, previous)
- Battery\-powered operation
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

