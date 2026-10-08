# 🎵 Pitch Finder

A browser-based **real-time pitch detection application** that listens through the microphone and identifies the musical note being sung or played.

## ✨ Features

- 🎤 Real-time microphone pitch detection
- 🎼 Musical note detection
- 📊 Frequency display in Hz
- 🎯 Tuning accuracy in cents
- 🎹 Piano-key visualization
- 🎵 Estimated song-key detection
- 📱 Responsive interface
- 🌐 Deployable as a web application
- 📦 Progressive Web App support

## 🛠️ Technology

- HTML5
- CSS3
- JavaScript
- Web Audio API
- `getUserMedia`
- Autocorrelation pitch detection

## 🧠 How It Works

```text
Microphone
    ↓
Audio Capture
    ↓
Web Audio API
    ↓
Autocorrelation
    ↓
Fundamental Frequency
    ↓
MIDI Note
    ↓
Musical Note + Tuning
```

The frequency is converted into a MIDI note using:

```text
MIDI = 69 + 12 × log₂(frequency / 440)
```

For example, `440 Hz → A4`.

## 🚀 Run Locally

```bash
git clone https://github.com/karunyakanth-lgtm/pitch-finder.git
cd pitch-finder
python -m http.server 8000
```

Open `http://localhost:8000` and allow microphone access.

## ⚠️ Limitations

- Background noise can reduce accuracy.
- Microphone quality affects results.
- Polyphonic audio is difficult to analyze accurately.
- Song-key estimation improves with more detected notes.

## 🔮 Future Improvements

- Better noise filtering
- Improved polyphonic detection
- Recording and playback
- Visual pitch graphs
- More accurate key estimation

## 👨‍💻 Author

**Karunya Kanth**  
First-year B.Tech CSE Student | Cybersecurity & Technology
