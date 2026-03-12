---
theme: seriph
layout: center
class: text-center
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: fade-out
title: SUBA - Evolución Arquitectónica
mdc: true
---

<div class="absolute inset-0 bg-white z-0"></div>

<div class="relative z-10 flex flex-col items-center justify-center h-full w-full">

  <div class="relative group">
    <div class="absolute inset-0 bg-blue-300 blur-3xl opacity-20 rounded-full group-hover:opacity-40 transition-opacity duration-700"></div>
    <img src="/logotipo.png" alt="Logotipo SUBA" class="h-48 object-contain relative hover:scale-105 transition-transform duration-700 drop-shadow-xl" />
  </div>

  <div class="mt-8 space-y-4">
    <h1 class="text-3xl font-black tracking-tight text-gray-800 drop-shadow-sm">
      Sistema Automatizado de <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-cyan-500">Boletería Urbana</span>
    </h1>
    <div class="text-gray-500 tracking-[0.2em] uppercase text-xs font-semibold">
      Evolución y Refactorización
    </div>
  </div>

  <div class="mt-16">
    <button @click="$slidev.nav.next" class="group relative px-8 py-3 font-bold text-white transition-all duration-300 rounded-xl overflow-hidden shadow-lg hover:shadow-blue-500/30">
      <span class="absolute inset-0 w-full h-full bg-gradient-to-r from-blue-600 to-cyan-500 opacity-90 group-hover:scale-105 transition-transform duration-500"></span>
      <span class="relative flex items-center gap-3 text-sm tracking-wide">
        INICIAR RECORRIDO <carbon-arrow-right class="animate-bounce-x text-lg" />
      </span>
    </button>
  </div>

</div>

<style>
.animate-bounce-x {
  animation: bounce-x 1.5s infinite;
}
@keyframes bounce-x {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(6px); }
}
</style>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Problemáticas del Transporte Público 🚩
<p class="text-gray-500 -mt-2 text-sm font-medium">Análisis de la situación actual y desafíos críticos</p>

<div class="grid grid-cols-2 gap-8 mt-10">
  <div v-click class="p-6 rounded-2xl bg-red-50 border border-red-100 shadow-sm text-left">
    <h3 class="text-red-600 font-bold mb-4 flex items-center gap-2 text-lg">
      <carbon:warning-alt-filled /> Crisis de Servicio
    </h3>
    <ul class="text-sm space-y-4 text-gray-700">
      <li class="flex items-start gap-3">
        <carbon:time class="text-red-500 mt-1 shrink-0" />
        <span><b>Incertidumbre:</b> Desconocimiento total de tiempos de llegada y disponibilidad de unidades.</span>
      </li>
      <li class="flex items-start gap-3">
        <carbon:currency class="text-red-500 mt-1 shrink-0" />
        <span><b>Fuga de Capital:</b> Sistemas de recaudación arcaicos sin trazabilidad financiera.</span>
      </li>
    </ul>
  </div>

  <div v-click class="p-6 rounded-2xl bg-orange-50 border border-orange-100 shadow-sm text-left">
    <h3 class="text-orange-600 font-bold mb-4 flex items-center gap-2 text-lg">
      <carbon:face-dissatisfied-filled /> Impacto Social y Gestión
    </h3>
    <p class="text-sm text-gray-700 leading-relaxed mb-4">
      <b>Obstáculos en el pago:</b> Proceso engorroso para obtener efectivo, billetes deteriorados y tarifas injustas/arbitrarias.
    </p>
    <div class="pt-4 border-t border-orange-200">
      <h4 class="font-bold text-xs text-orange-700 uppercase mb-2 flex items-center gap-1">
        <carbon:settings-adjust /> Ineficiencia Administrativa
      </h4>
      <p class="text-[11px] text-gray-600">
        Falta de coordinación entre entes, reformas de roles sin sustento técnico y ausencia de registros digitales (conductores, buses y rutas).
      </p>
    </div>
  </div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Antecedentes: Macro a Micro 🌍
<p class="text-gray-500 -mt-2 text-sm font-medium">Evolución y respuestas globales ante la crisis del transporte</p>

<div class="grid grid-cols-3 gap-4 mt-8">
  <div v-click class="p-4 rounded-xl bg-blue-50 border border-blue-100 shadow-sm">
    <h3 class="text-blue-700 font-bold mb-2 flex items-center gap-2 text-sm">
      <carbon:earth-filled /> Internacional
    </h3>
    <p class="text-[10px] text-gray-700 leading-relaxed">
      La digitalización en <b>Taiwán y Nueva York</b> ha eliminado cuellos de botella financieros. El transporte automatizado es el eje motor del desarrollo económico.
    </p>
  </div>

  <div v-click class="p-4 rounded-xl bg-emerald-50 border border-emerald-100 shadow-sm">
    <h3 class="text-emerald-700 font-bold mb-2 flex items-center gap-2 text-sm">
      <carbon:map-boundary /> Latinoamérica
    </h3>
    <p class="text-[10px] text-gray-700 leading-relaxed">
      Respuesta a la fuga de capital e ineficiencia. Urgencia de formalizar el sector para obtener <b>control estadístico total</b> y eliminar el sesgo en la planificación.
    </p>
  </div>

  <div v-click class="p-4 rounded-xl bg-yellow-50 border border-yellow-100 shadow-sm">
    <h3 class="text-yellow-700 font-bold mb-2 flex items-center gap-2 text-sm">
      <carbon:location-filled /> Venezuela
    </h3>
    <p class="text-[10px] text-gray-700 leading-relaxed">
      Experiencias como <b>VeTICKET y BTR</b> enfrentan falta de financiamiento. SUBA propone tecnología <i>Open Source</i> para mitigar la incertidumbre y profesionalizar la gestión.
    </p>
  </div>
</div>

<div v-click class="mt-8 grid grid-cols-3 gap-4">
  <div class="flex items-center gap-3 p-3 bg-gray-50 rounded-lg border border-gray-200">
    <span class="text-lg font-black text-gray-300">01</span>
    <p class="text-[10px] font-bold text-gray-600">Reducción de brecha financiera</p>
  </div>
  <div class="flex items-center gap-3 p-3 bg-gray-50 rounded-lg border border-gray-200">
    <span class="text-lg font-black text-gray-300">02</span>
    <p class="text-[10px] font-bold text-gray-600">Control estadístico real</p>
  </div>
  <div class="flex items-center gap-3 p-3 bg-gray-50 rounded-lg border border-gray-200">
    <span class="text-lg font-black text-gray-300">03</span>
    <p class="text-[10px] font-bold text-gray-600">Tecnología sostenible</p>
  </div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Planteamiento del Problema 🔍
<p class="text-gray-500 -mt-2 text-sm font-medium">Contexto geográfico y operativo del Estado Bolívar</p>

<div class="grid grid-cols-2 gap-8 mt-10">
  <div v-click class="p-6 rounded-2xl bg-blue-50 border border-blue-100 shadow-sm text-left">
    <h3 class="text-blue-600 font-bold mb-4 flex items-center gap-2 text-lg">
      <carbon:location-hazard /> Problemática Central
    </h3>
    <p class="text-sm text-gray-700 leading-relaxed">
      El transporte público en Bolívar opera bajo un <b>esquema arcaico</b> que ignora la gestión de tiempos, dejando al ciudadano en una incertidumbre total sin estimaciones de espera ni trazabilidad.
    </p>
    <div class="mt-6 p-4 bg-blue-600 bg-opacity-10 border-l-4 border-blue-600 rounded-r-lg">
      <p class="text-xs italic text-blue-900">"¿En qué medida SUBA permitirá optimizar el recaudo y la gestión de tiempos en este contexto?"</p>
    </div>
  </div>

  <div class="space-y-4">
    <div v-click class="flex items-start gap-3 p-3 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
      <carbon:error class="text-red-500 mt-1 shrink-0" />
      <p class="text-xs text-gray-700"><b>Ceguera Institucional:</b> El IMTTV carece de datos estadísticos para planificación vial y fiscalización real.</p>
    </div>
    <div v-click class="flex items-start gap-3 p-3 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
      <carbon:flash-off class="text-red-500 mt-1 shrink-0" />
      <p class="text-xs text-gray-700"><b>Brecha Digital:</b> Fracaso de iniciativas previas por falta de adaptabilidad a las limitaciones de conectividad local.</p>
    </div>
    <div v-click class="flex items-start gap-3 p-3 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
      <carbon:group-resource class="text-red-500 mt-1 shrink-0" />
      <p class="text-xs text-gray-700"><b>Desarticulación:</b> Ausencia de un canal de comunicación efectivo entre conductores, usuarios y entes reguladores.</p>
    </div>
  </div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Justificación del Proyecto 💡
<p class="text-gray-500 -mt-2 text-sm font-medium">¿Por qué es urgente implementar SUBA ahora?</p>

<div class="grid grid-cols-3 gap-6 mt-12">
  <div v-click class="p-5 rounded-2xl bg-blue-50 border border-blue-100 text-center shadow-sm">
    <carbon:iot-platform class="text-3xl text-blue-600 mb-4 mx-auto" />
    <h4 class="font-bold text-sm mb-2 text-blue-800">Técnica</h4>
    <p class="text-[10px] text-gray-600 leading-tight">Transición necesaria hacia la digitalización, integrando IoT y Big Data para resolver la logística urbana.</p>
  </div>

  <div v-click class="p-5 rounded-2xl bg-emerald-50 border border-emerald-100 text-center shadow-sm">
    <carbon:group-presentation class="text-3xl text-emerald-600 mb-4 mx-auto" />
    <h4 class="font-bold text-sm mb-2 text-emerald-800">Social</h4>
    <p class="text-[10px] text-gray-600 leading-tight">Dignificación del usuario al eliminar la incertidumbre y democratizar el acceso a la tecnología móvil.</p>
  </div>

  <div v-click class="p-5 rounded-2xl bg-purple-50 border border-purple-100 text-center shadow-sm">
    <carbon:enterprise class="text-3xl text-purple-600 mb-4 mx-auto" />
    <h4 class="font-bold text-sm mb-2 text-purple-800">Institucional</h4>
    <p class="text-[10px] text-gray-600 leading-tight">Fiscalización basada en reportes digitales veraces, permitiendo una planificación urbana eficiente.</p>
  </div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Hoja de Ruta: Objetivos 🎯
<p class="text-gray-500 -mt-2 text-sm font-medium">Metas estratégicas para la transformación del servicio</p>

<div class="mt-8 space-y-8">
  
<div v-click class="flex items-center gap-6 p-6 bg-blue-50 rounded-2xl border border-blue-100 shadow-sm">
  <div class="shrink-0 w-16 h-16 rounded-full bg-blue-600 flex items-center justify-center text-white text-3xl shadow-md">
    <carbon:rocket />
  </div>
  <div>
    <h4 class="font-bold text-blue-800 text-lg mb-1">Objetivo General</h4>
    <p class="text-sm text-gray-700 leading-relaxed">Desarrollar una solución tecnológica integral para solventar las deficiencias actuales del sistema de transporte en el municipio a través de un prototipo funcional.</p>
  </div>
</div>

<div class="grid grid-cols-2 gap-x-8 gap-y-4">
  
<div v-click class="flex items-start gap-3 p-4 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
  <div class="p-1 bg-blue-100 rounded-md shrink-0 mt-0.5">
    <carbon:search class="text-blue-600" />
  </div>
  <div>
    <p class="text-[12px] text-gray-700 leading-tight"><b>Diagnosticar</b> la situación actual del transporte público y sus puntos de dolor.</p>
  </div>
</div>
    
<div v-click class="flex items-start gap-3 p-4 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
  <div class="p-1 bg-emerald-100 rounded-md shrink-0 mt-0.5">
    <carbon:settings-check class="text-emerald-600" />
  </div>
  <div>
    <p class="text-[12px] text-gray-700 leading-tight"><b>Determinar</b> los requerimientos técnicos funcionales, no funcionales y el flujo del sistema.</p>
  </div>
</div>
    
<div v-click class="flex items-start gap-3 p-4 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
  <div class="p-1 bg-purple-100 rounded-md shrink-0 mt-0.5">
    <carbon:building class="text-purple-600" />
  </div>
  <div>
    <p class="text-[12px] text-gray-700 leading-tight"><b>Definir</b> la arquitectura de software robusta y los patrones de diseño aplicados.</p>
  </div>
</div>
    
<div v-click class="flex items-start gap-3 p-4 bg-gray-50 rounded-xl border border-gray-100 shadow-sm">
  <div class="p-1 bg-orange-100 rounded-md shrink-0 mt-0.5">
    <carbon:data-connected class="text-orange-600" />
  </div>
  <div>
    <p class="text-[12px] text-gray-700 leading-tight"><b>Integrar</b> datos en concordancia con el IMTTV/INTTV para responder a la ineficiencia operativa.</p>
  </div>
</div>

</div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# ¿Qué es SUBA? <span class="text-blue-600">🚌</span>
<p class="text-gray-500 -mt-2 text-sm font-medium">Una plataforma integral para modernizar el transporte en Ciudad Bolívar.</p>

<div class="grid grid-cols-2 gap-10 mt-12">
  <div v-click class="group p-6 rounded-2xl bg-blue-50 border border-blue-100 shadow-sm hover:shadow-md transition-all duration-500 hover:-translate-y-2">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
      <carbon:user-avatar class="text-2xl text-blue-600" />
    </div>
    <h3 class="text-xl font-bold mb-3 text-blue-800">Módulo Pasajero</h3>
    <ul class="text-sm space-y-3 text-gray-700">
      <li class="flex items-center gap-2"><carbon:location-filled class="text-blue-500" /> Rastreo en tiempo real</li>
      <li class="flex items-center gap-2"><carbon:qr-code class="text-blue-500" /> Pagos digitales QR/NFC</li>
      <li class="flex items-center gap-2"><carbon:map class="text-blue-500" /> Rutas dinámicas e inteligentes</li>
    </ul>
  </div>

  <div v-click class="group p-6 rounded-2xl bg-orange-50 border border-orange-100 shadow-sm hover:shadow-md transition-all duration-500 hover:-translate-y-2">
    <div class="w-12 h-12 bg-orange-100 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
      <carbon:user-identification class="text-2xl text-orange-600" />
    </div>
    <h3 class="text-xl font-bold mb-3 text-orange-800">Módulo Conductor</h3>
    <ul class="text-sm space-y-3 text-gray-700">
      <li class="flex items-center gap-2"><carbon:currency-dollar class="text-orange-500" /> Recaudación automatizada</li>
      <li class="flex items-center gap-2"><carbon:radar class="text-orange-500" /> Telemetría constante</li>
      <li class="flex items-center gap-2"><carbon:analytics class="text-orange-500" /> Gestión de rendimiento</li>
    </ul>
  </div>
</div>

---
layout: center
class: text-center bg-white
---

<div class="absolute top-0 left-0 w-full h-full bg-white z-[-1]"></div>

<h3 class="text-gray-400 font-bold tracking-[0.3em] uppercase text-sm mb-4">El Corazón de la App</h3>
<h2 class="text-5xl font-black mb-16 text-gray-800">Stack Tecnológico <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-cyan-500">v2.0</span></h2>

<div class="flex justify-center items-center gap-8">
  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-white shadow-md rounded-2xl flex items-center justify-center mb-3 border border-gray-100 group-hover:border-blue-400 group-hover:shadow-blue-100 transition-all duration-300">
      <carbon:logo-react class="text-3xl text-blue-500" />
    </div>
    <span class="text-xs font-bold text-gray-600">React Native</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-white shadow-md rounded-2xl flex items-center justify-center mb-3 border border-gray-100 group-hover:border-green-500 group-hover:shadow-green-100 transition-all duration-300">
      <carbon:database-mongodb class="text-3xl text-green-600" />
    </div>
    <span class="text-xs font-bold text-gray-600">MongoDB</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-white shadow-md rounded-2xl flex items-center justify-center mb-3 border border-gray-100 group-hover:border-emerald-400 group-hover:shadow-emerald-100 transition-all duration-300">
      <carbon:cloud-services class="text-3xl text-emerald-500" />
    </div>
    <span class="text-xs font-bold text-gray-600">Supabase</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-white shadow-md rounded-2xl flex items-center justify-center mb-3 border border-gray-100 group-hover:border-purple-500 group-hover:shadow-purple-100 transition-all duration-300">
      <carbon:api class="text-3xl text-purple-600" />
    </div>
    <span class="text-xs font-bold text-gray-600">Fastify API</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-white shadow-md rounded-2xl flex items-center justify-center mb-3 border border-gray-100 group-hover:border-orange-500 group-hover:shadow-orange-100 transition-all duration-300">
      <carbon:event class="text-3xl text-orange-500" />
    </div>
    <span class="text-xs font-bold text-gray-600">MQTT Real-time</span>
  </div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Identidad Visual: Inspiración y Color 🎨
<p class="text-gray-500 -mt-2 text-sm font-medium">Construcción de marca y psicología del color aplicada</p>

<div class="grid grid-cols-2 gap-8 mt-10">
  
<v-click>
<div class="flex flex-col items-center">
  <div class="rounded-2xl overflow-hidden shadow-xl border border-gray-100">
    <img src="/imagenes/Logo2.jpg" class="h-64 object-contain" />
  </div>
  <p class="mt-4 text-xs font-bold text-gray-400 uppercase tracking-widest">Paleta de Colores y Recursos</p>
</div>
</v-click>

<div class="space-y-6">

<v-click>
<div class="p-6 rounded-2xl bg-blue-50 border border-blue-100 shadow-sm">
  <h3 class="text-blue-700 font-bold mb-3 flex items-center gap-2">
    <carbon:color-palette /> Elección Cromática
  </h3>
  <p class="text-sm text-gray-700 leading-relaxed">
    Uso de los colores de la <b>identidad nacional</b> (Amarillo, Azul y Rojo) adaptados a un entorno tecnológico. El azul profundo transmite <b>confianza y seguridad</b>, mientras que el naranja/amarillo evoca <b>energía y movimiento</b>.
  </p>
</div>
</v-click>

<v-click>
<div class="p-6 rounded-2xl bg-gray-50 border border-gray-100 shadow-sm">
  <h3 class="text-gray-700 font-bold mb-3 flex items-center gap-2">
    <carbon:idea /> Concepto del Isotipo
  </h3>
  <p class="text-sm text-gray-600 leading-relaxed italic">
    Un diseño dinámico que integra la silueta de la unidad de transporte con líneas de velocidad, simbolizando la modernización y fluidez que SUBA aporta a Ciudad Bolívar.
  </p>
</div>
</v-click>
    
<v-click>
<div class="flex justify-center">
  <img src="/imagenes/Logo.jpg" class="h-16 object-contain opacity-80" />
</div>
</v-click>

</div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Marca Oficial y Wireframes 📐
<p class="text-gray-500 -mt-2 text-sm font-medium">Del concepto a la estructura de la aplicación</p>

<div class="grid grid-cols-2 gap-8 mt-10 items-stretch">
  
<v-click>
  <div class="flex flex-col items-center justify-center p-8 bg-gray-50 rounded-2xl border border-gray-200 shadow-sm h-full">
    <img src="/imagenes/Logo.jpg" alt="Logo Oficial SUBA" class="w-full max-w-[250px] object-contain" />
    <p class="mt-8 text-xs font-bold text-gray-400 uppercase tracking-widest">Isotipo Final</p>
  </div>
</v-click>

<v-click>
  <div class="flex flex-col items-center justify-center p-4 bg-gray-50 rounded-2xl border border-gray-200 shadow-sm h-full">
    <img src="/imagenes/wildfrend.jpg" alt="Wireframes SUBA" class="w-full h-auto object-contain rounded-xl shadow-inner" />
    <p class="mt-4 text-xs font-bold text-gray-400 uppercase tracking-widest">Estructura y Flujos (Wireframes)</p>
  </div>
</v-click>

</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Interfaz de Usuario: SUBA App 📱
<p class="text-gray-500 -mt-2 text-sm font-medium">Experiencia móvil moderna, intuitiva y funcional</p>

<div class="grid grid-cols-6 gap-3 mt-6">
  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-md border border-gray-200">
      <img src="/imagenes/1.png" class="w-full object-cover" />
    </div>
    <p class="text-[10px] text-center font-bold text-blue-600 uppercase">Login</p>
  </div>
  
  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-md border border-gray-200">
      <img src="/imagenes/2.png" class="w-full object-cover" />
    </div>
    <p class="text-[10px] text-center font-bold text-blue-600 uppercase">Home</p>
  </div>

  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-md border border-gray-200">
      <img src="/imagenes/3.png" class="w-full object-cover" />
    </div>
    <p class="text-[10px] text-center font-bold text-blue-600 uppercase">Billetera</p>
  </div>

  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-md border border-gray-200">
      <img src="/imagenes/4.png" class="w-full object-cover" />
    </div>
    <p class="text-[10px] text-center font-bold text-blue-600 uppercase">Perfil</p>
  </div>

  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-md border border-gray-200">
      <img src="/imagenes/5.png" class="w-full object-cover" />
    </div>
    <p class="text-[10px] text-center font-bold text-blue-600 uppercase">Subsidios</p>
  </div>

  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-md border border-gray-200">
      <img src="/imagenes/6.png" class="w-full object-cover" />
    </div>
    <p class="text-[10px] text-center font-bold text-blue-600 uppercase">Mapa</p>
  </div>
</div>

<div v-click class="mt-8 p-4 bg-blue-50 border border-blue-100 rounded-2xl">
  <p class="text-[11px] text-gray-600 text-center italic leading-tight">
    "Diseño centrado en la usabilidad del ciudadano bolivarense, priorizando la claridad visual y la eficiencia en la gestión de tiempos y pagos."
  </p>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Evolución de Mapas: Data-Driven 🗺️
<p class="text-gray-500 -mt-2 text-sm font-medium">Flujo de datos geoespaciales desde la API hasta el renderizado móvil</p>

<div class="grid grid-cols-2 gap-6 mt-8">
  
<div class="space-y-4">
  
<div v-click class="p-4 bg-blue-50 border border-blue-100 rounded-xl shadow-sm">
  <h4 class="text-xs font-bold text-blue-800 flex items-center gap-2 mb-2">
    <carbon:api /> 1. Petición a la API
  </h4>
  <p class="text-[10px] text-gray-700 leading-tight">La aplicación utiliza la función <code>fetchActiveRoutes</code> para consultar el endpoint <code>/api/rutas/activas</code> y obtener la información actualizada.</p>
</div>

<div v-click class="p-4 bg-emerald-50 border border-emerald-100 rounded-xl shadow-sm">
  <h4 class="text-xs font-bold text-emerald-800 flex items-center gap-2 mb-2">
    <carbon:data-1 /> 2. Datos Obtenidos
  </h4>
  <ul class="text-[10px] text-gray-700 leading-tight list-disc pl-4 space-y-1">
    <li><b>Puntos clave:</b> Inicio, fin y paradas intermedias.</li>
    <li><b>Geometría:</b> El campo <code>geometry</code> contiene el trazado exacto en formato <b>GeoJSON</b> para dibujar la ruta.</li>
  </ul>
</div>

</div>

<div class="space-y-4">
  
<div v-click class="p-4 bg-orange-50 border border-orange-100 rounded-xl shadow-sm">
  <h4 class="text-xs font-bold text-orange-800 flex items-center gap-2 mb-2">
    <carbon:store /> 3. Gestión de Paradas
  </h4>
  <p class="text-[10px] text-gray-700 leading-tight">Consulta al endpoint <code>/api/paradas/activas</code>. Se guardan en caché local (<b>AsyncStorage</b>) con vigencia de 24h para carga ultrarrápida.</p>
</div>

<div v-click class="p-4 bg-purple-50 border border-purple-100 rounded-xl shadow-sm">
  <h4 class="text-xs font-bold text-purple-800 flex items-center gap-2 mb-2">
    <carbon:screen /> 4. Visualización
  </h4>
  <p class="text-[10px] text-gray-700 leading-tight">La información se inyecta en un <b>WebView</b> (navegador interno) que renderiza el mapa interactivo utilizando los assets locales <code>map.html</code> y <code>map2.html</code>.</p>
</div>

</div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Ecosistema Financiero <span class="text-yellow-500">💳</span>
<p class="text-gray-500 -mt-2 text-sm font-medium">Transacciones seguras y sin contacto</p>

<div class="grid grid-cols-3 gap-6 mt-10">
  <div v-click class="p-4 rounded-xl bg-blue-50 border border-blue-100 text-center shadow-sm">
    <carbon:wallet class="text-3xl text-blue-600 mb-2 mx-auto" />
    <h4 class="font-bold mb-1 text-blue-800">Smart Wallet</h4>
    <p class="text-[10px] text-gray-600 leading-tight">Recargas vía Pago Móvil con validación de capturas y P2P instantáneo.</p>
  </div>

  <div v-click class="p-4 rounded-xl bg-emerald-50 border border-emerald-100 text-center shadow-sm">
    <carbon:qr-code class="text-3xl text-emerald-600 mb-2 mx-auto" />
    <h4 class="font-bold mb-1 text-emerald-800">Pagos QR</h4>
    <p class="text-[10px] text-gray-600 leading-tight">Generación dinámica de tokens de abordaje para pasajeros sin NFC.</p>
  </div>

  <div v-click class="p-4 rounded-xl bg-orange-50 border border-orange-100 text-center shadow-sm">
    <carbon:wireless-checkout class="text-3xl text-orange-600 mb-2 mx-auto" />
    <h4 class="font-bold mb-1 text-orange-800">Tecnología NFC</h4>
    <p class="text-[10px] text-gray-600 leading-tight">Vinculación de tarjetas físicas para pagos offline (Sin batería/Internet).</p>
  </div>
</div>

<div v-click class="mt-10 p-6 rounded-2xl bg-gray-50 border border-gray-200 shadow-sm">
  <h3 class="text-gray-800 font-bold mb-2 flex items-center gap-2 text-sm uppercase">
    <carbon:license-maintenance class="text-blue-600" /> Gestión de Subsidios
  </h3>
  <p class="text-xs text-gray-600 leading-relaxed">
    Integración de módulo de verificación para <b>Estudiantes, Adultos Mayores y Discapacidad</b>. 
    Carga de constancias directamente a Supabase Storage con flujo de aprobación administrativa.
  </p>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Panel Administrativo: Control Financiero 💻
<p class="text-gray-500 -mt-2 text-sm font-medium">Gestión centralizada de recargas, aprobaciones e historial</p>

<div class="grid grid-cols-2 gap-6 mt-8">
  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-lg border border-gray-200">
      <img src="/imagenes/8.png" class="w-full object-cover" />
    </div>
    <p class="text-xs text-center font-bold text-gray-600 uppercase tracking-wide">Gestión de Transferencias</p>
    <p class="text-[10px] text-center text-gray-500 px-4">Verificación y aprobación de recargas con comprobante bancario.</p>
  </div>

  <div v-click class="space-y-2">
    <div class="rounded-xl overflow-hidden shadow-lg border border-gray-200">
      <img src="/imagenes/9.png" class="w-full object-cover" />
    </div>
    <p class="text-xs text-center font-bold text-gray-600 uppercase tracking-wide">Historial y Auditoría</p>
    <p class="text-[10px] text-center text-gray-500 px-4">Trazabilidad completa de todas las transacciones procesadas.</p>
  </div>
</div>

<div v-click class="mt-6 p-4 bg-gray-50 border border-gray-200 rounded-xl flex items-center justify-between">
  <div class="flex items-center gap-3">
    <carbon:security class="text-2xl text-blue-600" />
    <div>
      <h4 class="text-sm font-bold text-gray-700">Seguridad y Transparencia</h4>
      <p class="text-[10px] text-gray-500">Métricas en tiempo real de saldos totales y aprobaciones pendientes.</p>
    </div>
  </div>
  <div class="flex gap-2">
    <span class="px-2 py-1 bg-green-100 text-green-700 text-[9px] font-bold rounded">Aprobaciones</span>
    <span class="px-2 py-1 bg-blue-100 text-blue-700 text-[9px] font-bold rounded">Métricas</span>
  </div>
</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Panel Administrativo: Gestión de Rutas 🗺️
<p class="text-gray-500 -mt-2 text-sm font-medium">Control espacial y trazado dinámico del transporte</p>

<div class="grid grid-cols-12 gap-6 mt-6 items-center">

<div class="col-span-5 space-y-4">

<div v-click class="p-3 bg-blue-50 rounded-xl border border-blue-100 flex items-start gap-3 shadow-sm">
  <div class="p-2 bg-blue-100 rounded-lg text-blue-600 shrink-0">
    <carbon:map class="text-xl" />
  </div>
  <div>
    <h4 class="text-xs font-bold text-blue-800">Constructor Interactivo</h4>
    <p class="text-[10px] text-gray-600 leading-tight mt-1">Trazado punto a punto sobre el mapa con cálculo automático de aristas OSRM.</p>
  </div>
</div>

<div v-click class="p-3 bg-emerald-50 rounded-xl border border-emerald-100 flex items-start gap-3 shadow-sm">
  <div class="p-2 bg-emerald-100 rounded-lg text-emerald-600 shrink-0">
    <carbon:location-star class="text-xl" />
  </div>
  <div>
    <h4 class="text-xs font-bold text-emerald-800">Control de Paradas</h4>
    <p class="text-[10px] text-gray-600 leading-tight mt-1">Definición de paradas, rutas circulares y bidireccionales en tiempo real.</p>
  </div>
</div>

<div v-click class="p-3 bg-orange-50 rounded-xl border border-orange-100 flex items-start gap-3 shadow-sm">
  <div class="p-2 bg-orange-100 rounded-lg text-orange-600 shrink-0">
    <carbon:data-format class="text-xl" />
  </div>
  <div>
    <h4 class="text-xs font-bold text-orange-800">Datos Geoespaciales</h4>
    <p class="text-[10px] text-gray-600 leading-tight mt-1">Generación automática de polilíneas GeoJSON para consumo del cliente móvil.</p>
  </div>
</div>

</div>

<div class="col-span-7">
<div v-click class="w-full rounded-2xl overflow-hidden shadow-xl border border-gray-200">
  <img src="/imagenes/7.png" alt="Gestión de Rutas Admin Panel" class="w-full h-auto object-cover" />
</div>
</div>

</div>

---
layout: default
---

<div class="absolute inset-0 bg-white z-[-1]"></div>

# Telemetría y Tiempo Real <span class="text-purple-600">📡</span>
<p class="text-gray-500 -mt-2 text-sm font-medium">Conectividad constante entre la flota y el usuario</p>

<div class="grid grid-cols-2 gap-10 mt-12">

<div class="space-y-6">

<div v-click class="flex items-center gap-4 p-4 bg-purple-50 rounded-2xl border border-purple-100 shadow-sm">

<div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center">
  <carbon:network-4 class="text-2xl text-purple-600" />
</div>

<div>
  <h4 class="font-bold text-sm text-purple-800">Protocolo MQTT (HiveMQ)</h4>
  <p class="text-[10px] text-gray-600 mt-1 leading-tight">Transmisión ultra-ligera de coordenadas cada 5s con consumo mínimo de datos.</p>
</div>

</div>

<div v-click class="flex items-center gap-4 p-4 bg-cyan-50 rounded-2xl border border-cyan-100 shadow-sm">

<div class="w-12 h-12 bg-cyan-100 rounded-xl flex items-center justify-center">
  <carbon:time class="text-2xl text-cyan-600" />
</div>

<div>
  <h4 class="font-bold text-sm text-cyan-800">Cálculo de ETA Dinámico</h4>
  <p class="text-[10px] text-gray-600 mt-1 leading-tight">Predicción de llegada basada en la velocidad real y distancias del motor OSRM.</p>
</div>

</div>

</div>

<div v-click class="relative">

<div class="absolute -top-3 left-4 px-3 py-1 bg-white border border-gray-200 shadow-sm rounded-lg text-[9px] font-mono text-gray-600 z-10 font-bold">
  bus_telemetry.json
</div>

<div class="p-6 pt-8 rounded-2xl bg-gray-50 border border-gray-200 shadow-md font-mono text-[11px] leading-relaxed">

<div class="flex gap-1.5 mb-4">
  <div class="w-2 h-2 rounded-full bg-red-400"></div>
  <div class="w-2 h-2 rounded-full bg-yellow-400"></div>
  <div class="w-2 h-2 rounded-full bg-green-400"></div>
</div>

<div class="text-gray-700">
  <span class="text-purple-600 font-bold">{</span><br>
  &nbsp;&nbsp;<span class="text-emerald-600">"bus_id"</span>: <span class="text-orange-600">"GU-104"</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-600">"latitude"</span>: <span class="text-blue-600">8.2799</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-600">"longitude"</span>: <span class="text-blue-600">-62.7299</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-600">"speed"</span>: <span class="text-blue-600">45.2</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-600">"status"</span>: <span class="text-orange-600">"active"</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-600">"route_id"</span>: <span class="text-orange-600">"6581f1..."</span><br>
  <span class="text-purple-600 font-bold">}</span>
</div>

</div>

</div>

</div>

---
layout: default
---

<div class="absolute inset-0 bg-white overflow-hidden">
  <div class="absolute top-[-20%] left-[-10%] w-96 h-96 bg-blue-300 blur-[120px] opacity-30 rounded-full"></div>
  <div class="absolute bottom-[-20%] right-[-10%] w-96 h-96 bg-emerald-300 blur-[120px] opacity-20 rounded-full"></div>
  <div class="absolute inset-0 bg-gradient-to-b from-blue-50/50 to-white/80"></div>
</div>

<div class="absolute inset-0 flex flex-col items-center justify-center z-10">
  
  <h1 class="text-8xl font-black mb-6 text-gray-800 drop-shadow-sm tracking-tight">
    ¡Gracias!
  </h1>
  
  <p class="text-2xl text-gray-500 font-bold tracking-[0.3em] uppercase flex items-center gap-6">
    <span class="w-16 h-[2px] bg-gray-300"></span> 
    Proyecto SUBA 
    <span class="w-16 h-[2px] bg-gray-300"></span>
  </p>
  
</div>
