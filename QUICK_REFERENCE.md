# ⚡ त्वरित संदर्भ - नमस्ते ट्यूब पार्टनर प्रोग्राम

## 🚀 अंदर 30 सेकंड में शुरू करें

### Firebase से क्या कॉपी करें?

```
Firebase Console → Project Settings → Your apps → </> 
↓
7 चीजें कॉपी करें:
1. apiKey
2. authDomain
3. databaseURL ← MOST IMPORTANT
4. projectId
5. storageBucket
6. messagingSenderId
7. appId
```

### index.html में कहां भरें?

```html
<!-- लाइन 276-283 में जाएं: -->
<script type="module">
    // ...
    const firebaseConfig = {
        apiKey: "यहां भरें",
        authDomain: "यहां भरें",
        databaseURL: "यहां भरें",  ⭐ सबसे महत्वपूर्ण
        projectId: "यहां भरें",
        storageBucket: "यहां भरें",
        messagingSenderId: "यहां भरें",
        appId: "यहां भरें"
    };
```

---

## 📋 फॉर्म फील्ड्स

| फील्ड | प्रकार | उदाहरण |
|------|------|--------|
| आपका नाम | Text | राज कुमार |
| ईमेल | Email | raj@youtube.com |
| फोन नंबर | 10 digits | 9876543210 |
| चैनल नाम | Text | मेरा चैनल |
| कंटेंट कैटेगरी | Dropdown | शिक्षा/संगीत/तकनीक |
| सदस्य संख्या | Number | 5000 |

---

## 🔒 Security Rules को कॉपी करें

Firebase Console में Rules टैब खोलें और यह चिपकाएं:

```json
{
  "rules": {
    "partner_applications": {
      ".read": true,
      ".write": true
    }
  }
}
```

**फिर "Publish" पर क्लिक करें**

---

## 🎨 रंग कस्टमाइज करें

लाइन 13-17 में:

```css
:root {
    --kesari: #FF9933;      /* केसरी - मुख्य रंग */
    --safed: #FFFFFF;       /* सफेद - टेक्स्ट */
    --hara: #138808;        /* हरा - सफलता */
    --dark-bg: #0a0e14;     /* डार्क - बैकग्राउंड */
}
```

---

## 🐛 अगर काम न करे?

| समस्या | समाधान |
|--------|--------|
| "Firebase is not defined" | सभी 7 values सही हैं? |
| डेटा सेव नहीं हो रहा | Rules में ".write": true है? |
| Form काम नहीं कर रहा | F12 Console में error देखें |
| फोन valid नहीं | 10 अंक होने चाहिए |

---

## 📱 मोबाइल टेस्टिंग

```
अपने फोन पर खोलने के लिए:
1. Local network पर अपना IP खोजें (ipconfig)
2. http://YOUR_IP:8000 पर जाएं
3. फॉर्म टेस्ट करें
```

---

## 📊 Firebase में डेटा देखना

```
Firebase Console
  → Realtime Database
    → Data tab
      → partner_applications
        → आपके entries
```

---

## 🌐 Deploy करने के लिए

### Vercel पर (सबसे आसान)

```bash
1. GitHub पर पुश करें
2. vercel.com पर जाएं
3. "Import Project"
4. अपना repo चुनें
5. Deploy!
```

### GitHub Pages पर

```bash
1. Settings → Pages
2. Source: main branch
3. /root से serve करें
4. अपना URL मिलेगा
```

### Firebase Hosting पर

```bash
npm install -g firebase-tools
firebase login
firebase init
firebase deploy
```

---

## 📝 HTML में नई फील्ड कैसे जोड़ें?

### Step 1: HTML में जोड़ें (लाइन ~330)

```html
<div class="form-group">
    <label for="new_field">नया लेबल *</label>
    <input type="text" id="new_field" name="new_field" required>
</div>
```

### Step 2: JavaScript में जोड़ें (लाइन ~343)

```javascript
const formData = {
    name: document.getElementById('name').value,
    // ... अन्य फील्ड
    new_field: document.getElementById('new_field').value,  // यह जोड़ें
};
```

---

## 🎯 Firebase Realtime Database Structure

```
Namaste-tube database
└── partner_applications/
    └── [Auto-generated ID]/
        ├── name: "राज कुमार"
        ├── email: "raj@example.com"
        ├── phone: "9876543210"
        ├── channel: "मेरा चैनल"
        ├── category: "शिक्षा"
        ├── subscribers: 5000
        └── timestamp: "2026-05-12T10:30:00Z"
```

---

## 🎬 Live Demo कैसे बनाएं?

```bash
# Option 1: सीधे खोलें
open index.html

# Option 2: Local Server
python -m http.server 8000
# फिर: http://localhost:8000

# Option 3: Python 3
python -m http.server

# Option 4: Node.js
npx http-server
```

---

## ✨ Pro Tips

1. **अपना logo बदलें:** लाइन 307 में 🙏 चेंज करें
2. **हेडर टाइटल बदलें:** लाइन 5 में बदलें
3. **Footer बदलें:** लाइन 353 में बदलें
4. **Language बदलें:** html lang="hi" को lang="en" करें
5. **Dark mode हटाएं:** CSS में colors बदलें

---

## 📚 उपयोगी Links

- [Firebase Docs](https://firebase.google.com/docs)
- [MDN - HTML Forms](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
- [CSS Glassmorphism](https://glassmorphism.com)
- [Google Fonts](https://fonts.google.com)

---

## ⏱️ समय अनुमान

| काम | समय |
|-----|------|
| Firebase Setup | 5 मिनट |
| Config भरना | 2 मिनट |
| Security Rules | 2 मिनट |
| Testing | 3 मिनट |
| **कुल** | **12 मिनट** |

---

## 🆘 Support Channels

1. **Firebase Console Errors:** F12 → Console Tab देखें
2. **Issues:** GitHub पर file करें
3. **Questions:** Discussions में पूछें
4. **Documentation:** README.md पढ़ें

---

**आखिरी अपडेट:** 2026-05-12  
**Version:** 1.0  
**Language:** हिंदी + English  
**License:** MIT

🙏 **नमस्ते!**
