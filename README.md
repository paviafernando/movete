# Movete 🤸 (prueba de concepto)

Juego de movimiento con la cámara: detecta el cuerpo (MediaPipe Pose, en el navegador) y los aros de colores sobre la alfombra, y pide poses y "twister" de aros.

- Un solo `index.html`, sin build. Necesita HTTPS (Vercel) para usar la cámara e internet para bajar el detector.
- Flujo: elegir modo y dificultad → prender cámara → (solo con "Aros en el piso" activado: buscar aros, tocar para sacar/sumar) → 8–12 retos con voz, estrellas y récord por dificultad.
- Retos: manos arriba, avión, manos en la cabeza, sapito, flamenco, estrella, rodillas, mano derecha/izquierda, parate en el aro X, tocá el aro X con la mano, un pie en X y otro en Y, combos.
- **Modo caras** 😜 (MediaPipe Face Landmarker con blendshapes): sonrisa, boca abierta, ojos cerrados, trompita, cachetes inflados, sorpresa, enojo, cejas arriba, guiño y triste. Barra de "fuerza" del gesto y un emoji espejo que copia la cara que ponés.
- **Modo máscaras** 🎭: emojis que siguen la cabeza y reaccionan a los gestos (se estiran con la boca, se inflan con los cachetes, rebotan al sonreír, largan corazones/brillitos/gotitas). Copiona, Gatito y Monito cambian de emoji según la cara. Botón "A jugar con la máscara" para jugar a las caras con la máscara puesta. Flechas ← → cambian de máscara.
- **Movimientos** (modo cuerpo): saltar, aplaudir, trepar como mono, correr en el lugar, sentadillas, aletear, abrir y cerrar las piernas, saltos de tijera, saludar y dar una vuelta; se cuentan las repeticiones. Poses nuevas: cintura, abrazo, corazón, señalar el techo, pie cruzado, estatua.
- **Dibujar con la mano** (Medio y Difícil): círculo, triángulo, cuadrado, corazón, zigzag, espiral, estrella e infinito, siguiendo puntitos; en Difícil con la mano derecha o izquierda.
- **Modo Baby** 👶 (1 a 2 años): burbujas para reventar con el cuerpo, música de cajita y consignas simples (aplaudir, avión, pajarito, arriba las manos, chau chau, ¿dónde está?, cabeza, panza, sapito, bailar, pisar fuerte). Nunca se pierde. Tira de arriba para que el adulto elija la actividad, ⏭ para pasar y 📌 para repetir siempre la misma. Una ⭐ por logro y gran festejo cada 3.
- **Look de videojuego**: fondo animado, esqueleto neón, estelas en las manos, muñequito con escenario en modo sin imagen, puntos con rachas (x2…x5), monedas y niveles que se guardan.
- **Tele + celu como cámara** 📺📱: la tele abre una sala (`?tv`, o `?hub=CODE` desde el índice) y muestra un QR; el celu entra con `?c=CODE`, detecta el cuerpo o la cara con MediaPipe y manda los puntos (datos) y la imagen (video) por WebRTC con PeerJS (sala `movete-tv-CODE`). La tele no necesita cámara.
- **Multijugador** 👥 (hasta 3): cada persona tiene color y animalito (🦄 🐯 🐸, de izquierda a derecha), puntos propios, bonus al primero que lo logra y podio al final. En Baby la consigna vale si la hace cualquiera y todos revientan burbujas; en Máscaras cada cara tiene su máscara.
- **Control remoto**: en la tele (o con `?tv`/`?hub`) cada botón muestra su número; los números del control lo activan (inicio: 1-4 modos, 5-7 dificultad, 8 jugadores, 9 sin imagen, 0 jugar; baby: 1-9 actividad, 0 siguiente; máscaras: 4/6 anterior/siguiente; final: 0 una más, 1 inicio) y "volver" va al inicio. CSS sin `inset`/`color-mix` para navegadores de tele.
- **Voz en el celu**: si la tele no tiene voces (o se elige "Habla: el celu"), la tele le manda las frases al celu-cámara y las dice el celu; en el celu hay que tocar "🔊 Activar voz" una vez.
- **Voz**: elige sola la voz más natural del dispositivo; el botón 🗣️ permite probar y elegir otra.
- **Sin imagen** 🙈: en vez de la cámara se ve un muñequito con la cabeza del emoji elegido.
- Vigilante: si la cámara o el detector se traban, se recuperan solos (y pasa a CPU si la GPU falla). `?debug` muestra valores, detecciones por segundo y errores.
- Publicado en https://movete-nine.vercel.app y visible en el índice.
