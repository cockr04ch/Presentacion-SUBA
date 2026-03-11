---
theme: seriph
background: https://images.unsplash.com/photo-1639322537228-f710d846310a?auto=format&fit=crop&q=80
class: text-center
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: fade-out
title: SUBA - Evolución Arquitectónica
mdc: true
---

# <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-600 font-extrabold">Proyecto SUBA</span>
<div class="flex justify-center my-6 relative">
  <div class="absolute inset-0 bg-blue-500 blur-3xl opacity-20 rounded-full"></div>
  <img src="/logotipo.png" alt="Logotipo SUBA" class="h-40 object-contain relative hover:scale-105 transition-transform duration-500" />
</div>

<h3 class="opacity-90 tracking-widest uppercase text-sm mb-2">Sistema Automatizado de Boletería Urbana</h3>

<div class="mt-4 flex justify-center gap-2 items-center">
  <span class="px-3 py-1 bg-blue-500 bg-opacity-20 border border-blue-400 border-opacity-30 rounded-full text-xs font-mono text-blue-300">
    v2.0.1 - Refactorización
  </span>
</div>

<div class="pt-12">
  <button @click="$slidev.nav.next" class="group relative px-6 py-2 font-medium text-white transition-all duration-300">
    <span class="absolute inset-0 w-full h-full bg-gradient-to-r from-blue-600 to-cyan-500 rounded-lg blur-sm group-hover:blur-md opacity-70"></span>
    <span class="relative flex items-center gap-2 text-sm">
      Comenzar Recorrido <carbon:arrow-right class="animate-bounce-x" />
    </span>
  </button>
</div>

<style>
.animate-bounce-x {
  animation: bounce-x 1s infinite;
}
@keyframes bounce-x {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(5px); }
}
</style>

---
layout: intro
---

# ¿Qué es SUBA? <span class="text-blue-400">🚌</span>

<p class="opacity-80 text-lg">Una plataforma integral para modernizar el transporte en Ciudad Bolívar.</p>

<div class="grid grid-cols-2 gap-10 mt-12">
  <div v-click class="group p-6 rounded-2xl bg-white bg-opacity-5 border border-white border-opacity-10 backdrop-blur-md hover:bg-opacity-10 transition-all duration-500 hover:-translate-y-2">
    <div class="w-12 h-12 bg-blue-500 bg-opacity-20 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
      <carbon:user-avatar class="text-2xl text-blue-400" />
    </div>
    <h3 class="text-xl font-bold mb-3 text-blue-300">Módulo Pasajero</h3>
    <ul class="text-sm space-y-3 opacity-70">
      <li class="flex items-center gap-2"><carbon:location-filled class="text-blue-500" /> Rastreo en tiempo real</li>
      <li class="flex items-center gap-2"><carbon:qr-code class="text-blue-500" /> Pagos digitales QR/NFC</li>
      <li class="flex items-center gap-2"><carbon:map class="text-blue-500" /> Rutas dinámicas e inteligentes</li>
    </ul>
  </div>

  <div v-click class="group p-6 rounded-2xl bg-white bg-opacity-5 border border-white border-opacity-10 backdrop-blur-md hover:bg-opacity-10 transition-all duration-500 hover:-translate-y-2">
    <div class="w-12 h-12 bg-orange-500 bg-opacity-20 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
      <carbon:user-identification class="text-2xl text-orange-400" />
    </div>
    <h3 class="text-xl font-bold mb-3 text-orange-300">Módulo Conductor</h3>
    <ul class="text-sm space-y-3 opacity-70">
      <li class="flex items-center gap-2"><carbon:currency-dollar class="text-orange-500" /> Recaudación automatizada</li>
      <li class="flex items-center gap-2"><carbon:radar class="text-orange-500" /> Telemetría constante</li>
      <li class="flex items-center gap-2"><carbon:analytics class="text-orange-500" /> Gestión de rendimiento</li>
    </ul>
  </div>
</div>

---
layout: default
---

# El Desafío: Realidad del Transporte 🚩
<p class="opacity-50 -mt-2 text-sm">Contexto geográfico y operativo del Estado Bolívar</p>

<div class="grid grid-cols-2 gap-8 mt-10">
  <div v-click>
    <h3 class="text-red-400 font-bold mb-4 flex items-center gap-2 text-lg">
      <carbon:warning-alt-filled /> Problemática Central
    </h3>
    <p class="text-sm opacity-80 leading-relaxed">
      El transporte público en Bolívar opera bajo un <b>esquema arcaico</b> que ignora la gestión de tiempos, dejando al ciudadano en una incertidumbre total sin estimaciones de espera ni trazabilidad.
    </p>
    <div class="mt-6 p-4 bg-red-500 bg-opacity-10 border-l-4 border-red-500 rounded-r-lg">
      <p class="text-xs italic">"¿En qué medida SUBA permitirá optimizar el recaudo y la gestión de tiempos en este contexto?"</p>
    </div>
  </div>

  <div class="space-y-4">
    <div v-click class="flex items-start gap-3">
      <carbon:close-outline class="text-red-500 mt-1 shrink-0" />
      <p class="text-xs opacity-70"><b>Fuga de Capitales:</b> Sistemas de pago basados exclusivamente en efectivo.</p>
    </div>
    <div v-click class="flex items-start gap-3">
      <carbon:close-outline class="text-red-500 mt-1 shrink-0" />
      <p class="text-xs opacity-70"><b>Ceguera Institucional:</b> El IMTTV carece de datos estadísticos para planificación vial.</p>
    </div>
    <div v-click class="flex items-start gap-3">
      <carbon:close-outline class="text-red-500 mt-1 shrink-0" />
      <p class="text-xs opacity-70"><b>Brecha Digital:</b> Fracaso de iniciativas previas por falta de adaptabilidad local.</p>
    </div>
  </div>
</div>

---
layout: default
---

# Justificación del Proyecto 💡
<p class="opacity-50 -mt-2 text-sm">¿Por qué es urgente implementar SUBA ahora?</p>

<div class="grid grid-cols-3 gap-6 mt-12">
  <div v-click class="p-5 rounded-2xl bg-blue-500 bg-opacity-5 border border-blue-500 border-opacity-20 text-center">
    <carbon:iot-platform class="text-3xl text-blue-400 mb-4 mx-auto" />
    <h4 class="font-bold text-sm mb-2 text-blue-200">Técnica</h4>
    <p class="text-[10px] opacity-60">Transición necesaria hacia la digitalización, integrando IoT y Big Data para resolver la logística urbana.</p>
  </div>

  <div v-click class="p-5 rounded-2xl bg-emerald-500 bg-opacity-5 border border-emerald-500 border-opacity-20 text-center">
    <carbon:group-presentation class="text-3xl text-emerald-400 mb-4 mx-auto" />
    <h4 class="font-bold text-sm mb-2 text-emerald-200">Social</h4>
    <p class="text-[10px] opacity-60">Dignificación del usuario al eliminar la incertidumbre y democratizar el acceso a la tecnología móvil.</p>
  </div>

  <div v-click class="p-5 rounded-2xl bg-purple-500 bg-opacity-5 border border-purple-500 border-opacity-20 text-center">
    <carbon:enterprise class="text-3xl text-purple-400 mb-4 mx-auto" />
    <h4 class="font-bold text-sm mb-2 text-purple-200">Institucional</h4>
    <p class="text-[10px] opacity-60">Fiscalización basada en reportes digitales veraces, permitiendo una planificación urbana eficiente.</p>
  </div>
</div>

---
layout: default
---

# Hoja de Ruta: Objetivos 🎯

<div class="mt-10 space-y-8">
  <div v-click class="flex items-center gap-6">
    <div class="shrink-0 w-14 h-14 rounded-full border-2 border-blue-500 flex items-center justify-center font-bold text-blue-400 text-xl">GO</div>
    <div>
      <h4 class="font-bold text-blue-300">Objetivo General</h4>
      <p class="text-sm opacity-70">Desarrollar un sistema basado en aplicación móvil para optimizar el control de recaudo y la gestión de tiempos en el transporte público del Estado Bolívar.</p>
    </div>
  </div>

  <div class="grid grid-cols-2 gap-x-12 gap-y-6">
    <div v-click class="flex gap-3">
      <carbon:checkmark-outline class="text-blue-500 shrink-0" />
      <p class="text-[11px] opacity-60"><b>Diagnosticar</b> fallas actuales y la ausencia de indicadores de tiempo.</p>
    </div>
    <div v-click class="flex gap-3">
      <carbon:checkmark-outline class="text-blue-500 shrink-0" />
      <p class="text-[11px] opacity-60"><b>Determinar</b> requerimientos técnicos considerando limitaciones de conectividad regional.</p>
    </div>
    <div v-click class="flex gap-3">
      <carbon:checkmark-outline class="text-blue-500 shrink-0" />
      <p class="text-[11px] opacity-60"><b>Diseñar</b> arquitectura de datos e interfaz UI/UX centrada en la simplicidad.</p>
    </div>
    <div v-click class="flex gap-3">
      <carbon:checkmark-outline class="text-blue-500 shrink-0" />
      <p class="text-[11px] opacity-60"><b>Validar</b> el sistema mediante pruebas de campo y simulaciones reales.</p>
    </div>
  </div>
</div>

---
layout: center
class: text-center
---

# <span class="opacity-50 text-2xl font-light tracking-tighter">EL CORAZÓN DE LA APP</span>
<h2 class="text-5xl font-black mb-16">Stack Tecnológico <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-cyan-500">v2.0</span></h2>

<div class="flex justify-center items-center gap-8">
  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-gray-800 rounded-2xl flex items-center justify-center mb-2 border border-gray-700 group-hover:border-blue-500 transition-all">
      <carbon:logo-react class="text-3xl text-blue-400" />
    </div>
    <span class="text-xs font-bold">React Native</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-gray-800 rounded-2xl flex items-center justify-center mb-2 border border-gray-700 group-hover:border-green-500 transition-all">
      <carbon:database-mongodb class="text-3xl text-green-500" />
    </div>
    <span class="text-xs font-bold">MongoDB</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-gray-800 rounded-2xl flex items-center justify-center mb-2 border border-gray-700 group-hover:border-emerald-500 transition-all">
      <carbon:cloud-services class="text-3xl text-emerald-400" />
    </div>
    <span class="text-xs font-bold">Supabase</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-gray-800 rounded-2xl flex items-center justify-center mb-2 border border-gray-700 group-hover:border-purple-500 transition-all">
      <carbon:api class="text-3xl text-purple-400" />
    </div>
    <span class="text-xs font-bold">Fastify API</span>
  </div>

  <div v-click class="flex flex-col items-center group">
    <div class="w-16 h-16 bg-gray-800 rounded-2xl flex items-center justify-center mb-2 border border-gray-700 group-hover:border-orange-500 transition-all">
      <carbon:event class="text-3xl text-orange-400" />
    </div>
    <span class="text-xs font-bold">MQTT Real-time</span>
  </div>
</div>

---
layout: default
---

# Evolución de Mapas <span class="text-cyan-400">🗺️</span>
<p class="opacity-50 -mt-2 text-sm">De la dependencia estática a la soberanía de datos</p>

<div class="grid grid-cols-2 gap-8 mt-8">
  <div v-click class="p-5 rounded-2xl bg-red-500 bg-opacity-5 border border-red-500 border-opacity-20">
    <h3 class="text-red-400 font-bold mb-4 flex items-center gap-2">
      <carbon:close-filled /> v1.0 (Limitaciones)
    </h3>
    <ul class="text-sm space-y-3 opacity-80">
      <li>❌ Rutas hardcodeadas en <code>Destinos.json</code></li>
      <li>❌ Consulta directa a Overpass (API Pública lenta)</li>
      <li>❌ Cálculo de ruta en el cliente (Alto consumo)</li>
      <li>❌ Sin soporte offline efectivo</li>
    </ul>
  </div>

  <div v-click class="p-5 rounded-2xl bg-emerald-500 bg-opacity-5 border border-emerald-500 border-opacity-20">
    <h3 class="text-emerald-400 font-bold mb-4 flex items-center gap-2">
      <carbon:checkmark-filled /> v2.0 (Arquitectura Data-Driven)
    </h3>
    <ul class="text-sm space-y-3 opacity-80">
      <li>✅ <b>API REST Propia:</b> Endpoints de rutas/paradas</li>
      <li>✅ <b>GeoJSON Pre-calculado:</b> Renderizado instantáneo</li>
      <li>✅ <b>Offline-First:</b> Caché local con <code>AsyncStorage</code></li>
      <li>✅ <b>Estilo Neón:</b> Visualización optimizada de trayectorias</li>
    </ul>
  </div>
</div>

---
layout: default
---

# Ecosistema Financiero <span class="text-yellow-400">💳</span>
<p class="opacity-50 -mt-2 text-sm">Transacciones seguras y sin contacto</p>

<div class="grid grid-cols-3 gap-6 mt-10">
  <div v-click class="p-4 rounded-xl bg-white bg-opacity-5 border border-white border-opacity-10 text-center">
    <carbon:wallet class="text-3xl text-blue-400 mb-2 mx-auto" />
    <h4 class="font-bold mb-1">Smart Wallet</h4>
    <p class="text-[10px] opacity-60">Recargas vía Pago Móvil con validación de capturas y P2P instantáneo.</p>
  </div>

  <div v-click class="p-4 rounded-xl bg-white bg-opacity-5 border border-white border-opacity-10 text-center">
    <carbon:qr-code class="text-3xl text-emerald-400 mb-2 mx-auto" />
    <h4 class="font-bold mb-1">Pagos QR</h4>
    <p class="text-[10px] opacity-60">Generación dinámica de tokens de abordaje para pasajeros sin NFC.</p>
  </div>

  <div v-click class="p-4 rounded-xl bg-white bg-opacity-5 border border-white border-opacity-10 text-center">
    <carbon:wireless-checkout class="text-3xl text-orange-400 mb-2 mx-auto" />
    <h4 class="font-bold mb-1">Tecnología NFC</h4>
    <p class="text-[10px] opacity-60">Vinculación de tarjetas físicas para pagos offline (Sin batería/Internet).</p>
  </div>
</div>

<div v-click class="mt-10 p-6 rounded-2xl bg-blue-600 bg-opacity-10 border border-blue-500 border-opacity-20">
  <h3 class="text-blue-300 font-bold mb-2 flex items-center gap-2 text-sm uppercase">
    <carbon:license-maintenance /> Gestión de Subsidios
  </h3>
  <p class="text-xs opacity-70 leading-relaxed">
    Integración de módulo de verificación para <b>Estudiantes, Adultos Mayores y Discapacidad</b>. 
    Carga de constancias directamente a Supabase Storage con flujo de aprobación administrativa.
  </p>
</div>

---
layout: default
---

# Telemetría y Tiempo Real <span class="text-purple-400">📡</span>
<p class="opacity-50 -mt-2 text-sm">Conectividad constante entre la flota y el usuario</p>

<div class="grid grid-cols-2 gap-10 mt-12">

<div class="space-y-6">

<div v-click class="flex items-center gap-4 p-4 bg-white bg-opacity-5 rounded-2xl border border-white border-opacity-10 backdrop-blur-sm">

<div class="w-12 h-12 bg-purple-500 bg-opacity-20 rounded-xl flex items-center justify-center">
  <carbon:network-4 class="text-2xl text-purple-400" />
</div>

<div>
  <h4 class="font-bold text-sm text-purple-200">Protocolo MQTT (HiveMQ)</h4>
  <p class="text-[10px] opacity-60">Transmisión ultra-ligera de coordenadas cada 5s con consumo mínimo de datos.</p>
</div>

</div>

<div v-click class="flex items-center gap-4 p-4 bg-white bg-opacity-5 rounded-2xl border border-white border-opacity-10 backdrop-blur-sm">

<div class="w-12 h-12 bg-cyan-500 bg-opacity-20 rounded-xl flex items-center justify-center">
  <carbon:time class="text-2xl text-cyan-400" />
</div>

<div>
  <h4 class="font-bold text-sm text-cyan-200">Cálculo de ETA Dinámico</h4>
  <p class="text-[10px] opacity-60">Predicción de llegada basada en la velocidad real y distancias del motor OSRM.</p>
</div>

</div>

</div>

<div v-click class="relative">

<div class="absolute -top-3 left-4 px-3 py-1 bg-gray-800 border border-gray-700 rounded-lg text-[9px] font-mono text-gray-400 z-10">
  bus_telemetry.json
</div>

<div class="p-6 pt-8 rounded-2xl bg-gray-900 border border-gray-800 shadow-2xl font-mono text-[11px] leading-relaxed">

<div class="flex gap-1.5 mb-4 opacity-30">
  <div class="w-2 h-2 rounded-full bg-red-500"></div>
  <div class="w-2 h-2 rounded-full bg-yellow-500"></div>
  <div class="w-2 h-2 rounded-full bg-green-500"></div>
</div>

<div class="text-gray-400">
  <span class="text-purple-400">{</span><br>
  &nbsp;&nbsp;<span class="text-emerald-400">"bus_id"</span>: <span class="text-orange-300">"GU-104"</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-400">"latitude"</span>: <span class="text-cyan-300">8.2799</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-400">"longitude"</span>: <span class="text-cyan-300">-62.7299</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-400">"speed"</span>: <span class="text-cyan-300">45.2</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-400">"status"</span>: <span class="text-orange-300">"active"</span>,<br>
  &nbsp;&nbsp;<span class="text-emerald-400">"route_id"</span>: <span class="text-orange-300">"6581f1..."</span><br>
  <span class="text-purple-400">}</span>
</div>

</div>

</div>

</div>

---
layout: statement
---

<div class="flex flex-col items-center">
  <carbon:quotes class="text-6xl opacity-20 mb-8" />
  <h1 class="text-6xl font-black tracking-tighter leading-tight">
    El código <span class="text-blue-500">estable</span><br>
    siempre vive en <span class="bg-blue-500 px-4 rounded-lg">main</span>.
  </h1>
  <p class="mt-12 opacity-50 uppercase tracking-[0.3em] text-sm">Metodología Gitflow Adaptada</p>
</div>

---
layout: default
---

# Disciplina de Desarrollo 🌿

<div class="grid grid-cols-2 gap-12 mt-10">
  <div>
    <h3 class="flex items-center gap-2 text-red-400 font-bold mb-4 uppercase text-xs tracking-widest">
      <carbon:rule class="text-lg" /> La Regla de Oro
    </h3>
    <div class="p-6 bg-red-500 bg-opacity-5 border border-red-500 border-opacity-20 rounded-2xl relative overflow-hidden group">
      <div class="absolute top-0 right-0 p-2 opacity-10 group-hover:scale-150 transition-transform">
        <carbon:warning-alt class="text-6xl text-red-500" />
      </div>
      <p class="relative z-10 text-lg leading-relaxed italic">
        "Prohibido el commit directo a <span class="text-red-500 font-bold">main</span>. La calidad se asegura mediante Pull Requests."
      </p>
    </div>
  </div>

  <div>
    <h3 class="flex items-center gap-2 text-blue-400 font-bold mb-4 uppercase text-xs tracking-widest">
      <carbon:tag class="text-lg" /> Nomenclatura Estándar
    </h3>
    <div class="bg-gray-900 rounded-xl p-4 font-mono text-sm border border-gray-800 shadow-2xl">
      <div class="flex gap-2 mb-3">
        <div class="w-3 h-3 rounded-full bg-red-500"></div>
        <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
        <div class="w-3 h-3 rounded-full bg-green-500"></div>
      </div>
      <p class="text-gray-400 mb-1">// Formato de rama</p>
      <p>
        <span class="text-purple-400">feature/</span><span class="text-yellow-400">[INICIALES]/</span><span class="text-emerald-400">tarea</span>
      </p>
      <div class="mt-4 pt-4 border-t border-gray-800">
        <p class="text-gray-500 text-[10px] mb-1">EJEMPLO:</p>
        <p class="text-blue-300">feature/JC/auth-biometric</p>
      </div>
    </div>
  </div>
</div>

---
layout: end
---

<div class="relative h-full flex flex-col items-center justify-center">
  <div class="absolute inset-0 bg-gradient-to-b from-blue-600/10 to-transparent"></div>
  
  <h1 class="text-7xl font-black mb-4">¡Gracias! <span class="text-yellow-400 italic">🇻🇪</span></h1>
  <p class="text-2xl opacity-60 font-light tracking-widest uppercase mb-12">Proyecto SUBA v2.0</p>

  <div class="flex gap-8">
    <a href="#" class="flex flex-col items-center group">
      <div class="w-16 h-16 bg-white bg-opacity-5 rounded-full flex items-center justify-center mb-2 group-hover:bg-blue-500 transition-all duration-500 shadow-xl border border-white border-opacity-10">
        <carbon:logo-github class="text-2xl" />
      </div>
      <span class="text-[10px] font-bold opacity-40 group-hover:opacity-100 transition-opacity uppercase tracking-widest">GitHub</span>
    </a>
    <a href="#" class="flex flex-col items-center group">
      <div class="w-16 h-16 bg-white bg-opacity-5 rounded-full flex items-center justify-center mb-2 group-hover:bg-emerald-500 transition-all duration-500 shadow-xl border border-white border-opacity-10">
        <carbon:document class="text-2xl" />
      </div>
      <span class="text-[10px] font-bold opacity-40 group-hover:opacity-100 transition-opacity uppercase tracking-widest">Docs</span>
    </a>
  </div>
</div>
