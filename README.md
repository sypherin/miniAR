# 📸 Real-Time Object Detection in the Browser (COCO-SSD + TensorFlow.js)

This simple web app turns any phone or laptop into a **real-time object detection scanner** — no cloud, no install, just the browser.
It uses TensorFlow.js and the COCO-SSD model to detect 80+ everyday objects directly on-device.

---

## 🧰 Features

* 🪄 Runs fully **in-browser** (no server inference needed)
* 📱 Works on most modern phones (Android, iPhone) and laptops
* 🔐 Private — no camera feed ever leaves your device
* 🪄 Real-time detection with bounding boxes and labels
* 🧠 Detects multiple objects per frame (up to 20+)

---

## 🚀 How to Run

### Run Directly on Your Phone (Termux)

1. Install [Termux](https://f-droid.org/en/packages/com.termux/).
2. Run:

   ```bash
   pkg update -y
   pkg install -y python
   termux-setup-storage
   cd ~/storage/downloads
   python -m http.server 8080 --bind 127.0.0.1
   ```
3. Open `http://localhost:8080` in Chrome on the same phone.
4. Tap “Start camera” — you’re live 🎥

---

## 🧠 Object Classes Detected

The COCO-SSD model can detect 80 common categories including:

* **People & transport**: person, car, bus, train, bicycle…
* **Indoor objects**: chair, couch, TV, laptop, keyboard…
* **Accessories**: cup, bottle, backpack, umbrella…
* **Animals**: dog, cat, bird, horse…
  (Full list available in the COCO dataset.)

---

## 🛠️ How to Tweak

* `model.detect(video, 20)` → increase max detections.
* Filter predictions by confidence score before drawing.
* Hook into detection data to trigger actions (e.g. count, log, alert).

---

## 🧭 Sample Output

```json
[
  { "class": "person", "score": 0.95, "bbox": [42, 81, 160, 320] },
  { "class": "cup", "score": 0.88, "bbox": [220, 200, 60, 90] }
]
```

---

## 💡 Ideas to Build On

* 🧾 Inventory scanner (warehouse / retail)
* 🧍 People + object co-occurrence → space utilization tracking
* 🧠 AR overlays and gesture control
* 🕵️ Anomaly detection: object appears / disappears over time
* 🕓 Pattern logging → surface hidden usage patterns

---

## 📜 License

MIT — use freely, modify, hack away.
TensorFlow.js & COCO-SSD are under their respective open-source licenses.
