# Ahorcado - Juego Interactivo en Español

Un juego clásico del ahorcado completamente en español, ¡Adivina la palabra antes de que se complete el dibujo!

## Características

- **110+ palabras en español** con pistas útiles
- **Diseño de cuaderno de cuadrícula** nostálgico y atractivo
- **Efectos de sonido** integrados (sin necesidad de archivos externos)
- **Totalmente responsive** - funciona en PC, tablets y móviles
- **Sistema anti-repetición** - no se repiten palabras hasta jugar todas
- **Doble input** - teclado virtual y teclado físico
- **Marcador persistente** - guarda tus mejores puntuaciones
- **Pistas contextuales** para cada palabra
- **6 oportunidades** con dibujo progresivo del ahorcado

## Demo en Vivo

Juega ahora: [https://galleto.github.io/ahorcado-web-game//](https://galleto.github.io/ahorcado-web-game/)

## Inicio Rápido

### Opción 1: Jugar en Línea
Simplemente visita el [demo en vivo](#demo-en-vivo) y comienza a jugar.

### Opción 2: Descargar y Jugar Localmente

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/galleto/ahorcado-web-game.git
   ```

2. **Abre el archivo**
   - Navega a la carpeta descargada
   - Abre `index.html` en tu navegador favorito

3. **¡Juega!**
   - No requiere instalación
   - No requiere servidor
   - Todo funciona offline

### Opción 3: Descargar ZIP
1. Haz clic en el botón verde **"Code"** arriba
2. Selecciona **"Download ZIP"**
3. Extrae el archivo
4. Abre `index.html` en tu navegador

## Cómo Jugar

### Reglas Básicas
1. Se muestra una palabra oculta con guiones bajos `_ _ _`
2. Lee la **pista** para ayudarte a adivinar
3. Selecciona letras usando el teclado en pantalla o tu teclado físico
4. Si aciertas, la letra aparece en verde y se revela en la palabra
5. Si fallas, la letra aparece en rojo y se agrega una parte al ahorcado
6. Tienes **6 intentos** antes de perder
7. ¡Adivina la palabra completa antes de que se dibuje todo el ahorcado!

### Controles
- **Teclado Virtual**: Haz clic en las letras en pantalla
- **Teclado Físico**: Presiona las teclas A-Z y Ñ directamente
- **Responsive**: Funciona perfectamente en touch screens

### Sistema de Puntuación
- **Aciertos**: Cuenta cuántas letras adivinaste correctamente
- **Errores**: Cuenta cuántas veces fallaste (máximo 6)
- Al terminar cada partida, puedes guardar tu puntuación con tu nombre
- El marcador guarda el Top 10 de todas las partidas
- **Importante**: Cada entrada en el marcador es una partida individual, no se actualiza por jugador
- Múltiples personas pueden jugar y cada una puede decidir si guarda o no su puntuación
- Ejemplo: Alex juega y guarda su puntuación, luego Alexa juega y puede elegir guardar la suya o no

## Tecnologías Utilizadas

- **HTML5** - Estructura semántica
- **CSS3** - Estilos modernos y animaciones
- **JavaScript Vanilla** - Lógica del juego (sin frameworks)
- **Canvas API** - Dibujo del ahorcado
- **Web Audio API** - Efectos de sonido
- **LocalStorage** - Persistencia de datos

## Características Técnicas

### Diseño Responsive
```css
/* Breakpoints */
- Desktop: > 768px
- Tablet: 480px - 768px
- Mobile: < 480px
- Small Mobile: < 360px
```

### Compatibilidad de Navegadores
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Opera 76+

### Rendimiento
- **Peso total**: ~40KB (archivo único)
- **Carga instantánea**: Sin dependencias externas
- **Optimizado**: Consumo mínimo de recursos
- **Offline-first**: Funciona sin internet después de cargar

### Sistema de Marcadores
- **Almacenamiento**: LocalStorage del navegador (local por dispositivo)
- **Capacidad**: Top 10 mejores puntuaciones
- **Persistencia**: Las puntuaciones se mantienen en el mismo navegador/dispositivo
- **Importante**: Cada dispositivo tiene su propio marcador independiente
- **No es compartido**: Si compartes el juego con otros, cada persona verá solo su marcador local
- **Funcionamiento**: Cada partida puede guardarse como una entrada independiente
- **No hay perfiles de usuario**: El sistema no asocia múltiples partidas al mismo nombre
- **Opcional**: Los jugadores pueden elegir no guardar su puntuación
- **Ordenamiento**: Se ordenan por mayor número de aciertos, y en caso de empate, por menor número de errores

## Palabras Incluidas

El juego incluye 110+ palabras cuidadosamente seleccionadas en categorías:

- **Sustantivos comunes**: Casa, árbol, familia, etc.
- **Verbos frecuentes**: Correr, pensar, hablar, etc.
- **Adjetivos**: Bonito, grande, rápido, etc.
- **Palabras con Ñ**: Año, niña, montaña, español, etc.

Cada palabra viene con una **pista descriptiva** para facilitar el juego.

## Sistema de Sonidos

Los sonidos se generan dinámicamente usando **Web Audio API**:

- **Acierto**: Nota musical agradable (Do - 523.25 Hz)
- **Error**: Nota grave (Sol - 196 Hz)
- **Victoria**: Melodía ascendente de 4 notas
- **Derrota**: Melodía descendente de 4 notas

*No requiere archivos de audio externos*

## Personalización

### Agregar Nuevas Palabras

Edita el array `palabras` en el código JavaScript:

```javascript
const palabras = [
    {word: "TuPalabra", hint: "Tu pista aquí"},
    // ... más palabras
];
```

### Cambiar Colores

Modifica las variables CSS en el `<style>`:

```css
/* Colores principales */
--primary-color: #3498db;
--success-color: #27ae60;
--error-color: #e74c3c;
```

### Ajustar Dificultad

Cambia el número de intentos:

```javascript
let maxWrong = 6; // Cambia a 5, 7, 8, etc.
```

## Estructura del Proyecto

```
ahorcado-juego/
│
├── index.html          # Archivo principal (HTML + CSS + JS)
├── README.md          # Este archivo
└── .gitignore         # Archivos ignorados por Git
```

## Contribuir

¡Las contribuciones son bienvenidas! Si quieres mejorar el juego:

1. **Fork** el repositorio
2. Crea una **rama** para tu feature (`git checkout -b feature/MejoraPro`)
3. **Commit** tus cambios (`git commit -m 'Agregar MejoraPro'`)
4. **Push** a la rama (`git push origin feature/MejoraPro`)
5. Abre un **Pull Request**

### Ideas para Contribuir
- Agregar más palabras
- Nuevos temas visuales
- Soporte para otros idiomas
- Niveles de dificultad
- Más estadísticas
- Música de fondo opcional

## Reportar Errores

Si encuentras un bug:

1. Ve a la sección **Issues**
2. Haz clic en **New Issue**
3. Describe el problema detalladamente
4. Incluye capturas de pantalla si es posible

## Preguntas Frecuentes

### ¿Cómo funciona el marcador?
El marcador guarda las mejores 10 puntuaciones de todas las partidas jugadas **en tu dispositivo específico**. Cada vez que terminas una partida, puedes ingresar tu nombre y guardar esa puntuación específica. No hay perfiles de usuario, por lo que si juegas varias veces con el mismo nombre, cada partida se guarda como una entrada separada.

### ¿Por qué no veo los marcadores de otras personas?
El marcador usa LocalStorage del navegador, lo que significa que **cada dispositivo tiene su propio marcador independiente**. Si compartes el link del juego con tu familia o amigos, cada uno verá solo sus propias puntuaciones en su dispositivo. No hay un servidor central que comparta los marcadores entre usuarios. Esto es intencional para mantener el juego simple y sin necesidad de backend.

### ¿Puedo ver los marcadores en otro dispositivo?
No, los marcadores están guardados localmente en cada dispositivo. Si juegas en tu computadora y luego en tu celular, cada uno tendrá marcadores diferentes. Para tener un marcador compartido entre dispositivos se necesitaría un servidor backend, lo cual está planeado para futuras versiones.

### ¿Puedo borrar el marcador?
Sí, el marcador se guarda en el LocalStorage de tu navegador. Puedes borrarlo limpiando los datos del sitio en la configuración de tu navegador, o puedes agregar un botón de reset modificando el código.

### ¿Las palabras se repiten?
No, el juego tiene un sistema anti-repetición. No se repetirá ninguna palabra hasta que hayas jugado las 110+ palabras disponibles. Una vez que completes todas, el sistema se reinicia automáticamente.

### ¿Necesito estar conectado a internet?
Funciona completamente offline ya que todo está en un solo archivo HTML.

### ¿Puedo agregar mis propias palabras?
Sí, puedes editar el archivo `index.html` y agregar palabras al array `palabras`. Cada palabra necesita un formato específico: `{word: "TuPalabra", hint: "Tu pista"}`.

### ¿Por qué no escucho sonidos?
Algunos navegadores bloquean el audio hasta que el usuario interactúe con la página. Intenta hacer clic en cualquier botón primero. Si el problema persiste, verifica que tu navegador tenga el audio habilitado.

## Si te Gusta

Si este proyecto te resultó útil o divertido:
- Dale una estrella al repositorio
- Compártelo con amigos
- Sígueme para más proyectos
---
