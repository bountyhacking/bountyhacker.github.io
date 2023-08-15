---
layout: post
title: "Tutorial Nmap Para Hackers EP 1"
img: nmap_banner.jpg # Add image post (optional) / size 1366x768
date: 2022-07-15 12:55:00 +0300
description: Aprende todo lo necesario para utilizar la herramienta de Nmap # Add post description (optional)
tag: [Video, Guia] # Video (cuando se sube a yt), Guia (explicar algo paso a paso), Articulo (hablar de algun tema de manera mas informal)
---

# Aprende todo lo necesario para utilizar la herramienta de Nmap

Una de las herramientas más utilizadas por los hackers y los ingenieros de redes, tanto como para auditorías internas como en competiciones Captrue The Flag (por sus siglas, C.T.F) es Nmap. Network mapper, o nmap es una poderoza y versátil herramienta de escaneo de puertos y posee una infinidad de opciones para aplicarlos hacia nuestros objetivos. Aprende a utilizar la herramienta número uno de los hackers para escanear tus objetivos en este video.

No olvides de leer las últimas noticias de la herramienta directamente desde su web: <a href="https://nmap.org">https://nmap.org.</a>

<iframe width="560" height="315" src="https://www.youtube.com/embed/zoOAnbVplSI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Nmap Cheat Sheed
Abajo encontrás una hoja de trucos (cheat sheed) sobre algunas técnicas de auditorías y recomendaciones de uso de la herramienta en entornos C.T.F...

### Escaneo Básico.
```bash
nmap -oA <file-name> <target-ip>
```

### Escaneo a Todos los Puertos.
```bash
nmap -p- <target-ip>
```

### Escaneo a Puertos Específicos.
```bash
nmap -p<ports> -oA <file-name> <target-ip>
```

### Escaneo a Rango de Puertos.
```bash
nmap -p<from_number>,<to_number> <target-ip>
```

### Escaneo a los Puertos Top 100
```bash
nmap -F <target-ip>
```

### Escaneo a Todos los Puertos.
```bash
nmap -p- -oA <file-name> <target-ip>
```

### Guardar los escaneos en todos los formatos (-oN, -oG, -oX).
```bash
nmap -oA <file-name> <target-ip>
```

### Técnicas de Optimización de Escaneos.
```bash
nmap -n -T5 --open <target-ip>
```

### Escaneos Para C.T.F - Primer Escaneo // Básico.
```bash
nmap --open -T5 -v -n <ip-target> -oA/oN/oG/oX <file-name>
```

### Escaneos Para C.T.F - Segundo Escaneo // Escaneo A Todos los Puertos.
```bash
nmap -p- --open -T5 -v -n <ip-target> -oA/oN/oG/oX <file-name>
```

### Escaneos Para C.T.F - Tercer Escaneo // Escaneo Avanzado Con Más Detalles.
```bash
nmap -p- -sS --min-rate 5000 --open -vvv -n <ip-target> -oA/oN/oG/oX <file-name>
```

### Escaneos Para C.T.F - Cuarto Escaneo // Explotando Las Versiones De Servicios y Sus Vulnerabilidades
```bash
nmap -sCV -p<port-number,range> -oA/oN/oG/oX <file-name>
```

Recuerda suscribirte al canal.

> Happy Hacking. <cite>- BountyHacker</cite>
