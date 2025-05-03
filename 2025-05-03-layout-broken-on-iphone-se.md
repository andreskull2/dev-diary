# 🛠️ Layout quebrava no iPhone SE (problema com 100vh)  
# 🛠️ _Layout broken on iPhone SE (100vh issue)_

**Data / _Date_:** 03/05/2025  
**Plataforma / _Platform_:** Projeto pessoal / CSS Puro  
**Situação / _Context_:**  
O layout apresentava problemas em dispositivos menores como o iPhone SE (1ª geração). A estrutura da página não respeitava o scroll e parte do conteúdo ficava escondida.  
_Layout was broken on smaller devices like the iPhone SE (1st gen). Page structure ignored scroll and some content was hidden._

---

## 🧪 Sintomas / _Symptoms_:

- Parte do conteúdo (como o footer) ficava invisível  
  _Some content (like the footer) was hidden_  
- A rolagem não funcionava corretamente  
  _Scrolling didn't behave properly_  
- Elementos pareciam cortados ou sobrepostos  
  _Elements appeared cut off or overlapping_

---

## 🕵️ Ações realizadas / _Steps taken_:

1. Analisei o CSS e identifiquei o uso de `height: 100vh` no `body`  
   _Inspected CSS and spotted `height: 100vh` used in `body`_  
2. Testei diferentes dispositivos no DevTools responsivo e em um iPhone SE real  
   _Tested across devices in DevTools and a real iPhone SE_  
3. Pesquisei sobre limitações do `100vh` em mobile  
   _Researched `100vh` limitations on mobile_

---

## 🧼 Solução aplicada / _Solution applied_:

- Substituí `height: 100vh` por `min-height: 100vh`  
  _Replaced `height: 100vh` with `min-height: 100vh`_  
- Adicionei `overflow-y: auto` ao `body` para permitir rolagem  
  _Added `overflow-y: auto` to `body` to allow scrolling_  
- Testei a rolagem e visibilidade do conteúdo → funcionou corretamente  
  _Tested scroll and content visibility → worked correctly_

---

## 📚 Aprendizado / _What I learned_:

`100vh` pode não funcionar como esperado em navegadores mobile, especialmente em iPhones com barras de navegação que somem/aparecem. `min-height: 100vh` é uma alternativa mais segura e `overflow-y: auto` garante rolagem adequada.  
_`100vh` may not behave as expected on mobile browsers, especially iPhones with dynamic nav bars. `min-height: 100vh` is a safer alternative, and `overflow-y: auto` ensures proper scrolling._

---

**Status:** ✅ Resolvido / _Resolved_  
**Tipo / _Type_:** CSS / Layout Mobile



