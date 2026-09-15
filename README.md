# 🚀 Flappy Rocket

A simple, beginner-friendly Flappy Bird game built in Python using **Pygame**, with an optional mobile-ready web edition.

---

## 🎮 How to Play

### 1. Run the Python Game (Desktop)
```bash
pip install pygame
python main.py
```
- **SPACE / UP / Screen Tap**: Fly (Thrust) / Start / Retry
- **H**: Toggle Hitbox Debug Mode (visualize hitboxes!)
- **R**: Restart when Game Over
- **ESC**: Exit

### 2. Run the Web Edition (Mobile & Browser)
- **Locally**: Double click `index.html` in your browser, or run:
  ```bash
  python app.py
  ```
  and open `http://localhost:5000`.
- **Deploy to Render**:
  - Full step-by-step instructions: see [RENDER_DEPLOY.md](RENDER_DEPLOY.md)
  - Connect your repo on [render.com](https://render.com)
  - Start Command: `gunicorn app:app`
  - Play on any phone or PC!

---

## 📂 Minimal Project Files

```
Flappy_Bird/
├── main.py            # The Python game (single clean file for students)
├── app.py             # Simple web server for Render (15 lines)
├── index.html         # Web edition (works in any browser & mobile)
├── requirements.txt   # Dependencies (pygame, Flask, gunicorn)
├── README.md          # This guide
└── assets/
    ├── images/        # rocket.png, obstacle.png, background.png
    └── sounds/        # ob-1.wav, lose-2.wav, thrust.wav, score.wav
```

---

## 🐛 Student Bug Hunt Exercise

> [!IMPORTANT]
> A deliberate collision bug is placed in [main.py](main.py) for students to find and fix!

1. Play the game and press **`H`** to turn on **Hitbox Debug Mode**.
2. Notice the **RED** collision box is slightly offset ahead of the **GREEN** rocket sprite!
3. Open `main.py`, search for:
   ```python
   # TODO: Fix collision/physics bug here
   ```
4. Adjust the collision box to match the true rocket position:
   ```python
   return pygame.Rect(self.x, self.y, self.width, self.height)
   ```
