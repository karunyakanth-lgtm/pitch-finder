# 🎵 Pitch Finder

A simple web-based **Pitch Finder** that listens through your microphone and detects the musical pitch you are singing or playing.

It shows the detected note, frequency, tuning accuracy, piano key, and an estimated song key.

## ✨ Features

- 🎤 Real-time microphone pitch detection
- 🎼 Detects musical notes such as C, D, E, F, etc.
- 📊 Displays frequency in Hz
- 🎯 Shows tuning accuracy in cents
- 🎹 Highlights the detected piano key
- 🎵 Estimates the key of the song
- ♯ Supports major and minor key detection
- 📱 Responsive design for mobile and desktop
- 🌐 Can be hosted as a web application
- 📦 Progressive Web App support

## 🛠️ Technologies Used

- HTML5
- CSS3
- JavaScript
- Web Audio API
- Microphone / `getUserMedia`
- Auto-correlation pitch detection

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/pitch-finder.git
cd pitch-finder
```

### 2. Run the project

Because microphone access requires a secure context, don't open the HTML file directly with `file://`.

You can use a local server such as VS Code Live Server.

Or with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

### 3. Allow microphone access

Click **Start Listening** and allow your browser to access the microphone.

> Microphone access works on `https://` websites or `localhost`.

## 🎯 How It Works

The application captures audio from the microphone using the Web Audio API.

The audio signal is analyzed using an **auto-correlation algorithm** to estimate the fundamental frequency.

The frequency is then converted into a MIDI note:

```text
MIDI = 69 + 12 × log₂(frequency / 440)
```

The detected MIDI value is converted into a musical note and octave.

The application also collects detected pitch classes and compares them with major and minor key profiles to estimate the song's key.

## 🎹 Example

If you sing or play a note close to:

```text
440 Hz
```

the application detects:

```text
A4
```

It also displays the tuning difference in cents.

## 📁 Project Structure

```text
pitch-finder/
│
├── index.html
├── manifest.webmanifest
├── sw.js
├── icon-192.png
└── README.md
```

## 🔐 Browser Permissions

Pitch Finder requires microphone permission to detect sound.

Your browser may ask for permission the first time you click **Start Listening**.

## ⚠️ Limitations

- Pitch detection depends on microphone quality.
- Background noise can affect detection accuracy.
- Polyphonic or complex audio may produce inaccurate results.
- Song-key estimation becomes more reliable after more notes are detected.
- Microphone access requires `localhost` or `HTTPS`.

## 🌐 Deployment

This project can be deployed using platforms such as:

- GitHub Pages
- Netlify
- Vercel

After deployment, open the HTTPS URL and allow microphone access.

## 👨‍💻 Author

**Karunya Kanth**

First-year Engineering Student  
Interested in **Cybersecurity, Technology and Software Development**

---

⭐ If you find this project useful, consider giving the repository a star!
