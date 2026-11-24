# Movete 🤸 (prueba de concepto)

Juego de movimiento con la cámara: detecta el cuerpo (MediaPipe Pose, en el navegador) y los aros de colores sobre la alfombra, y pide poses y "twister" de aros.

- Un solo `index.html`, sin build. Necesita HTTPS (Vercel) para usar la cámara e internet para bajar el detector.
- Flujo: elegir dificultad → prender cámara → buscar aros (tocar para sacar/sumar) → 8–12 retos con voz, estrellas y récord por dificultad.
- Retos: manos arriba, avión, manos en la cabeza, sapito, flamenco, estrella, rodillas, mano derecha/izquierda, parate en el aro X, tocá el aro X con la mano, un pie en X y otro en Y, combos.
- **Modo caras** 😜 (MediaPipe Face Landmarker con blendshapes): sonrisa, boca abierta, ojos cerrados, trompita, cachetes inflados, sorpresa, enojo, cejas arriba, guiño y triste. Barra de "fuerza" del gesto y un emoji espejo que copia la cara que ponés.
- Oculto en el índice (`"hidden": true`) hasta que deje de ser prueba.
