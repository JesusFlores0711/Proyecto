Nombre: JuegoBlackjack  
Definición de Variables:  
Lista: mazo, mano_jugador, mano_dealer  
Entero: puntaje_jugador, puntaje_dealer  
Texto: respuesta

1. Inicio
2. Barajar mazo
3. mano_jugador
4. mano_dealer

**Turno del jugador:**

5. Escribir "Tus cartas son: ", mano_jugador
6. Mientras calcular_puntaje(mano_jugador) < 21 Hacer
    7. Escribir "Tu puntaje es: ", calcular_puntaje(mano_jugador)
    8. Escribir "¿Quieres otra carta? (si/no)"
    9. Leer respuesta
    10. Si respuesta = "si" Entonces
        11. nueva_carta <- repartir carta del mazo
        12. Añadir nueva_carta a mano_jugador
        13. Escribir "Nueva carta: ", nueva_carta
    14. Fin Si
15. Fin Mientras

**Turno del dealer (si el jugador no se pasa de 21):**

16. Si calcular_puntaje(mano_jugador) <= 21 Entonces
    17. Escribir "Cartas del dealer: ", mano_dealer[0], " y carta oculta"
    18. Mientras calcular_puntaje(mano_dealer) < 17 Hacer
        19. nueva_carta <- repartir carta del mazo
        20. Añadir nueva_carta a mano_dealer
        21. Escribir "Dealer saca: ", nueva_carta
    22. Fin Mientras
    23. Escribir "Cartas del dealer: ", mano_dealer
24. Fin Si

**Comparar puntajes y determinar ganador:**

25. puntaje_jugador <- calcular_puntaje(mano_jugador)
26. puntaje_dealer <- calcular_puntaje(mano_dealer)
27. Si puntaje_jugador > 21 Entonces
    28. Escribir "Te pasaste de 21. Pierdes."
Sino
    29. Si puntaje_dealer > 21 Entonces
        30. Escribir "El dealer se pasó de 21. Ganaste."
    Sino
        31. Si puntaje_jugador > puntaje_dealer Entonces
            32. Escribir "¡Ganaste con ", puntaje_jugador, " puntos!"
        Sino
            33. Si puntaje_jugador < puntaje_dealer Entonces
                34. Escribir "El dealer ganó con ", puntaje_dealer, " puntos."
            Sino
                35. Escribir "Empate."
            Fin Si
        Fin Si
    Fin Si
Fin Si

36. Fin
