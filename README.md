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
- **Voz**: elige sola la voz más natural del dispositivo; el botón 🗣️ permite probar y elegir otra.
- **Sin imagen** 🙈: en vez de la cámara se ve un muñequito con la cabeza del emoji elegido.
- Vigilante: si la cámara o el detector se traban, se recuperan solos (y pasa a CPU si la GPU falla). `?debug` muestra valores, detecciones por segundo y errores.
- Publicado en https://movete-nine.vercel.app y visible en el índice.
