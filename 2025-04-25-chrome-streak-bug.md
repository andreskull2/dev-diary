# 🛠️ Chrome não exibia streak de estudos (Rocketseat)  
# 🛠️ _Chrome didn't show study streak (Rocketseat)_

**Data / _Date_:** 25/04/2025  
**Plataforma / _Platform_:** Rocketseat Fullstack  
**Situação / _Context_:**  
No Chrome, o ícone de ofensiva (🔥) da plataforma não aparecia, embora funcionasse normalmente no Safari e Opera.  
_In Chrome, the platform's streak icon (🔥) was missing, although it worked normally in Safari and Opera._

---

## 🧪 Sintomas / _Symptoms_:
- Ícone da ofensiva não carregava  
  _Streak icon did not load_  
- Console apresentava os erros:  
  _Console showed the following errors_:

```
Failed to load resource: net::ERR_HTTP2_PROTOCOL_ERROR  
Error fetching streaks: TypeError: network error  
```

---

## 🕵️ Ações realizadas / Steps taken:
1. Abri o DevTools (`Cmd + Option + I`)  
   _Opened DevTools_ (`Cmd + Option + I`)  
2. Analisei o console: falha de rede via protocolo HTTP/2  
   _Checked the console: HTTP/2 network failure_  
3. Testei em outros navegadores → funcional no Safari e Opera  
   _Cross-tested in other browsers → working in Safari and Opera_  
4. Verifiquei extensões → apenas Acrobat e Google Docs instaladas  
   _Checked extensions → only Acrobat and Google Docs installed_

---

## 🧼 Solução aplicada / _Solution applied_:
- Limpei **somente o cache** (`Imagens e arquivos armazenados em cache`)  
  _Cleared **only the cache**_ (`Cached images and files`)  
- Reiniciei o Chrome  
  _Restarted Chrome_  
- A ofensiva voltou a aparecer normalmente  
  _The streak icon came back normally_

---

## 📚 Aprendizado / _What I learned_:
Mesmo quando parece ser um bug da plataforma, pode ser problema de cache local. O DevTools ajuda muito a identificar a real causa. Reiniciar o navegador após a limpeza garantiu que tudo funcionasse.  
_Even when it seems like a platform bug, it might be just a local cache issue. DevTools helps a lot to spot the real cause. Restarting the browser after clearing cache solved the issue._

---

**Status:** ✅ Resolvido / _Resolved_  
**Tipo / _Type_:** Rede / Frontend | _Network / Frontend_