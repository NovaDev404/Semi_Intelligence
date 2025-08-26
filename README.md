# ⚡ SI Chatbot Engine

**INSTANT. TINY. LIGHTWEIGHT.**  
A JavaScript-based chatbot system built for speed, minimal footprint, and smart responses — no server, no bloat, just semi-smartness! 🧠✨

---

## 😜 Try it now!

Click [here](https://supergamer474.github.io/Semi_Intelligence/demo/) to try Semi Intelligence right here, right now!

### ⚡ Quick Start (30 seconds)
```bash
# Clone the repo
git clone https://github.com/SuperGamer474/Semi_Intelligence.git
cd Semi_Intelligence

# Start local server
python -m http.server 8000

# Open http://localhost:8000/demo in your browser
# Start chatting immediately! 🚀
```

---

## 💾 Key Features

- ⚡ **Instant**: Loads and replies in milliseconds — even on a potato 🥔
- 📦 **Tiny**: Uses a single JSON file as the model (kilobytes only!)
- 🧠 **Lightweight**: Minimal RAM usage — runs smoothly on *anything*, even low-spec devices
- 🪄 **Dynamic**: Smart placeholder functions like `{{name}}`, `{{timeOfDay}}`, and `{{randomEmoji}}`
- 🧰 **Offline-first**: 100% client-side. No APIs. No Internet. Works everywhere.
- 🔄 **Model Switching**: Switch between different AI personalities on the fly
- 🎯 **Error Resilient**: Graceful fallbacks and helpful error messages

---

## 💬 Models

- Download models from the releases page to test Semi Intelligence!
- The `R` in the models stands for `Responses`, which means how many topics it can respond to!
- The more responses the smarter the SI model is.
  
> ### Jacob - 6R
> Jacob is your go-to SI model if you just want super-light, personalised responses, with snappy greetings, quick jokes and friendly farewells.

> ### Alex - 44R
> Alex is best for rich, context-aware conversations that adapt to your name, time and mood—delivering personalised greetings, fun facts, jokes and helpful insights across topics!

> ### Norman - 98R
> Norman is best for smart, topic-spanning chats that personalise by name and time, thoughtful insights and responses across **many** subjects.

If you’re after casual chat, I recommend Alex for its friendly tone, varied replies and intelligent insights.

---

## 📁 File Structure
```
Semi_Intelligence/
├── SI.js              # Core chatbot engine (lightweight & powerful)
├── SI.html            # Main chat interface with model switching
├── README.md          # This documentation
└── demo/              # Ready-to-use demo
    ├── index.html     # Simple demo interface
    ├── Alex_44R.json  # 44-response AI model (recommended)
    ├── Jacob_6R.json  # 6-response lightweight model
    └── Norman_98R.json # 98-response advanced model
```

---

## 🚀 Get Started

### Quick Start (Local Demo)
1. **Clone or download** this repository
2. **Navigate to the demo folder**: `cd demo/`
3. **Start a local server**: `python -m http.server 8000` (or use any static file server)
4. **Open your browser** to `http://localhost:8000`
5. **Start chatting** with the pre-loaded Alex model!

### Using Your Own Models
1. **Download models** from the [releases section](https://github.com/SuperGamer474/Semi_Intelligence/releases)
2. **Place model files** in your project directory
3. **Load the model** in your JavaScript:
   ```javascript
   import { loadModel, get_si_response } from './SI.js';
   
   // Load a model
   await loadModel('./your-model.json');
   
   // Get a response
   const response = await get_si_response('Hello there!');
   console.log(response); // "Hi! How can I help you today?"
   ```

### Custom Model Creation
Create your own model by following this JSON structure:
```json
{
  "functions": {
    "name": "() => localStorage.getItem('name') || 'friend'",
    "timeOfDay": "() => { const h = new Date().getHours(); return h < 12 ? 'morning' : h < 18 ? 'afternoon' : 'evening'; }"
  },
  "greetings": ["hello", "hi", "hey"],
  "responses_greetings": ["Hi {{name}}! Good {{timeOfDay}}!", "Hello there!"],
  "response_map": {
    "greetings": "responses_greetings"
  },
  "unsure_responses": ["I'm not sure about that.", "Could you rephrase?"]
}
```

---

## 🪶 Ideal For:

- Semi-smart in-browser assistants 💬  
- Lightweight NPC dialogue in games 🎮  
- Offline tools or interactive lessons 📚  
- Anywhere you need basic *instant*, *tiny*, and *low-RAM* logic ⚡

---

## 🔧 Troubleshooting

### Common Issues

**🚨 "Model not loaded" error:**
- Ensure you're running a local server (not opening HTML files directly)
- Check that the model JSON file exists in the correct path
- Verify the file is valid JSON format

**💻 Demo not working:**
- Make sure you're in the `demo/` folder when starting the server
- Try a different port: `python -m http.server 3000`
- Check browser console for detailed error messages

**🤖 Bot not responding:**
- Check if the model file contains the required fields (`response_map`, keywords, responses)
- Verify your input matches keywords in the model
- Try basic greetings like "hello" first

### Performance Tips
- Use smaller models (like Jacob 6R) for faster loading
- Cache models locally instead of loading from remote URLs
- Minimize placeholder functions for better performance

---

## ⚠️ Important Warning

**Semi Intelligence is JUST that — semi-intelligent!**  
It’s super fast and lightweight, but it will often get stuff wrong or misunderstand you.  
Use it for fun, learning, and simple chats — but don’t expect a perfect AI genius yet! 🤖💥

---

## 🧙‍♂️ Created by

**[SuperGamer474](https://supergamer474.rf.gd/home/)**

---

## 📜 License

MIT — Free for personal, educational, or commercial use.  
Credit is appreciated, not required. 🙌
