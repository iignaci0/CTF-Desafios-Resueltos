# Desafíos CTF resueltos

**Integrante:** Ignacio Araya Becker

**Asignatura:** Ciberseguridad Avanzada

**Profesor:** Rodrigo Alejandro Ledezma Jaime

**Fecha de entrega:** 05/11/2026

---

Acá dejo resueltos los desafíos CTF del ramo, los que armaron los compañeros. La idea no era
solo sacar la FLAG y listo, sino entender qué hace cada herramienta mientras la voy usando,
porque varias no las había tocado nunca. Cada carpeta tiene su propio informe con el paso a
paso, los comandos, las capturas, dónde me enredé y qué saqué en limpio.

## Los desafíos

| # | Desafío | Herramienta principal | Lo que había que sacar |
|---|---------|----------------------|------------------------|
| 1 | La evidencia perdida | `file` y `strings` | 2 FLAG escondidas en un archivo |
| 2 | El registro perdido | Netcat (`nc`) | 1 FLAG hablándole a un servicio |
| 3 | Cracking de contraseñas | John the Ripper y Hashcat | 2 contraseñas (un .zip y un hash) |
| 4 | Captura de login | Wireshark / `tshark` | las credenciales que viajan en claro |
| 5 | ORION-7 | gobuster | 1 FLAG en 3 pedazos, enumerando un sitio |
| 6 | La FLAG perdida | Burp Suite | 1 FLAG entrando a un panel sin la clave |

Cada desafío está en su carpeta (`01-...`, `02-...`, etc.) con un `README.md` que es el informe,
y una subcarpeta `evidencias/` con las salidas de consola de verdad y las capturas.

## Dónde lo hice

Casi todo lo corrí en **Ubuntu dentro de WSL** (el Linux que se puede tener dentro de Windows),
porque los desafíos están pensados para Linux y ahí tengo `file`, `strings`, `nc`, `tshark`,
`python3` y `openssl` sin instalar nada raro. Para John, Hashcat y gobuster usé las herramientas
de verdad (no inventé las salidas), y ORION-7 lo levanté con Docker adentro de la misma WSL.

## Nota ética

Todo esto lo hice sobre desafíos de práctica, en mi propio equipo o sobre el sitio que el mismo
desafío decía atacar; nada fuera del ejercicio. Las mismas técnicas contra un sistema ajeno sin
permiso son delito, así que la idea es aprender a defenderse, no a hacer daño.

## Lo que me llevo

Lo más entretenido fue darme cuenta de que la mayoría de estos ataques no son "magia de hacker",
sino usar bien una herramienta simple y fijarse en detalles que uno pasaría por alto: una extensión
que miente, un puerto abierto, una clave débil, datos que viajan sin cifrar, una carpeta que nadie
enlazó o un campo de login que confía demasiado en lo que uno escribe. Entendiendo cómo se rompe,
queda mucho más claro cómo se protege. Eso sería lo principal.
