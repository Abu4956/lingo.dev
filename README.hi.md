⚡ Lingo.dev

Lingo.dev एक ओपन-सोर्स, एआई-संचालित  (अंतर्राष्ट्रीयकरण) टूलकिट है, जो LLMs की मदद से किसी भी ऐप को तुरंत बहुभाषी (multilingual) बनाता है।
---
🧩 Lingo.dev Compiler • CLI • CI/CD • SDK

रिलीज़ • लाइसेंस • आखिरी कमिट • Product Hunt उपलब्धियाँ:

-🥇 DevTool of the Month

-🥇 DevTool of the Week

-🥈 Product of the Day

-📈 GitHub Trending

---

🆕 Compiler से मिलिए

Lingo.dev Compiler एक मुफ़्त और ओपन-सोर्स कम्पाइलर मिडलवेयर है जो किसी भी React ऐप को बिल्ड टाइम पर बहुभाषी बनाता है — बिना आपके React कॉम्पोनेंट्स में कोई बदलाव किए।

इंस्टॉलेशन:
```bash
npm install lingo.dev
```

बिल्ड कॉन्फ़िगरेशन में जोड़ें:
```javascript
import lingoCompiler from "lingo.dev/compiler";

const existingNextConfig = {};

export default lingoCompiler.next({
  sourceLocale: "en",
  targetLocales: ["es", "fr"],
})(existingNextConfig);
```


अब ```next build``` चलाएँ और देखें — स्पैनिश और फ्रेंच बिल्ड अपने-आप तैयार हो जाएँगे! ✨

📘 पूरा गाइड पढ़ें: डॉक्यूमेंटेशन देखें और सहायता के लिए हमारे Discord सर्वर से जुड़ें।

---

📦 इस रिपॉज़िटरी में क्या है?

| टूल          | सारांश                                                                | डॉक्यूमेंटेशन |
| ------------ | -------------------------------------------------------------------|----------- |
| **Compiler** | बिल्ड टाइम पर React ऐप का अनुवाद                                     | `/compiler`   |
| **CLI**      | वेब और मोबाइल ऐप, JSON, YAML, markdown आदि के लिए एक कमांड से अनुवाद | `/cli`        |
| **CI/CD**    | हर पुश पर ऑटोमेटिक अनुवाद और कमिट                                    | `/ci`         |
| **SDK**      | यूज़र द्वारा जनरेट किए गए कंटेंट का रियलटाइम अनुवाद                  | `/sdk`        |

---

⚡️ Lingo.dev CLI

टर्मिनल से सीधे कोड और कंटेंट का अनुवाद करें:
```bash
npx lingo.dev@latest run
```


यह हर स्ट्रिंग को फिंगरप्रिंट करता है, रिजल्ट्स को कैश में रखता है, और केवल वही स्ट्रिंग्स दोबारा ट्रांसलेट करता है जो बदली हों।

📖 सेटअप गाइड: CLI डॉक्यूमेंटेशन देखें।

---

🔄 Lingo.dev CI/CD

हर push पर स्वचालित रूप से परफेक्ट अनुवाद भेजें 🚀

GitHub Actions सेटअप उदाहरण:
```yaml
# .github/workflows/i18n.yml
name: Lingo.dev i18n
on: [push]

jobs:
  i18n:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: lingodotdev/lingo.dev@main
        with:
          api-key: ${{ secrets.LINGODOTDEV_API_KEY }}
```

इससे आपका रिपॉज़िटरी हमेशा अपडेटेड और मल्टीलिंगुअल रहेगा 🌍

📘 पूरा गाइड: CI/CD डॉक्यूमेंटेशन पढ़ें।

---

🧩 Lingo.dev SDK

डायनामिक कंटेंट के लिए प्रति रिक्वेस्ट रियलटाइम अनुवाद।
```javascript
import { LingoDotDevEngine } from "lingo.dev/sdk";

const lingoDotDev = new LingoDotDevEngine({
  apiKey: "your-api-key-here",
});

const content = {
  greeting: "Hello",
  farewell: "Goodbye",
  message: "Welcome to our platform",
};

const translated = await lingoDotDev.localizeObject(content, {
  sourceLocale: "en",
  targetLocale: "es",
});

// आउटपुट:
// { greeting: "Hola", farewell: "Adiós", message: "Bienvenido a nuestra plataforma" }
```

यह चैट, यूज़र कमेंट्स, और अन्य रियलटाइम कंटेंट के लिए परफेक्ट है।

📖 पूरा गाइड: SDK डॉक्यूमेंटेशन देखें।

---

🤝 कम्युनिटी

हम एक कम्युनिटी-ड्रिवन प्रोजेक्ट हैं और योगदानों का स्वागत करते हैं ❤️

-💡 कोई आइडिया है? → Issue खोलें

-🔧 कुछ ठीक करना चाहते हैं? → PR भेजें

-💬 मदद चाहिए? → हमारे Discord सर्वर से जुड़ें

---

⭐ Star History

अगर आपको हमारा काम पसंद आया, तो हमें ⭐ दें
और हमें 4,000 स्टार तक पहुँचने में मदद करें! 🌟

---

🌐 अन्य भाषाओं में Readme

English • 中文 • 日本語 • 한국어 • Español • Français • Русский • Українська • Deutsch • Italiano • العربية • עברית • हिन्दी • বাংলা • فارسی

अपनी भाषा नहीं दिख रही?
i18n.json में जोड़ें और Pull Request भेजें! ✨
