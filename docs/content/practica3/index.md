+++
date = '2025-11-27T17:15:22-08:00'
draft = false
title = 'Practica3: Instalación de entorno de desarrollo Haskell y aplicación TODO'
+++

# **Práctica 3:** Instalación de entorno de desarrollo Haskell y aplicación TODO

## **Objetivo**

Instalar el entorno de desarrollo de Haskell, conocer sus herramientas principales y analizar el funcionamiento de una aplicación práctica desarrollada en este lenguaje, comprendiendo los fundamentos del paradigma funcional.

---

## **Desarrollo**

### **Primera sesión: Instalación del entorno**

1. Se ingresó a la página oficial de descargas de Haskell y se seleccionó el vínculo **Downloads**.  
2. Se identificó que la instalación se realiza mediante **GHCup**, una herramienta que gestiona el entorno de desarrollo.  
3. Se accedió al enlace de GHCup, desde donde se copió el comando de instalación para Windows.  
4. El comando se ejecutó en una ventana de PowerShell (sin modo administrador).  
5. Durante la instalación, GHCup descargó los siguientes componentes:  
   - **GHCup:** herramienta de gestión del entorno.  
   - **GHC:** compilador principal del lenguaje.  
   - **Hugs:** intérprete interactivo.  
   - **HLS (Haskell Language Server):** servidor de lenguaje para editores como VSCode.  
   - **Stack:** manejador de paquetes y proyectos.  
   - **Cabal:** herramienta de compilación y empaquetado.  
6. Se verificó la instalación ejecutando en PowerShell los comandos:  
   - `ghc --version`  
   - `stack --version`  
   - `ghcup --version`  
7. Finalmente, se revisó la guía oficial **Get Started** para confirmar el correcto funcionamiento del entorno y realizar las primeras pruebas del lenguaje.

---

### **Segunda sesión: Exploración del lenguaje y aplicación TODO**

1. Se revisó la guía **“Haskell Tutorial for C programmers”**, que explica los fundamentos de Haskell desde la perspectiva de un programador en C.  
2. Se estudió el **tour de sintaxis de Haskell** del departamento de CSE de Chalmers, comprendiendo el uso de funciones, listas, recursión, tipos y expresiones.  
3. Posteriormente, se analizó la **aplicación TODO App**, disponible en el blog oficial de Haskell.  
   - La aplicación permite agregar, listar y eliminar tareas desde la terminal.  
   - Fue desarrollada utilizando **Stack** para gestionar dependencias y compilar el proyecto.  
   - Implementa conceptos del paradigma funcional, como funciones puras, inmutabilidad y composición.  
4. Se ejecutó el ejemplo de la aplicación para verificar su funcionamiento y comprender la estructura de un proyecto en Haskell.

---

## **Conclusión**

Durante las dos sesiones se logró instalar y configurar correctamente el entorno de desarrollo de Haskell mediante GHCup, con todas sus herramientas integradas.  
Además, se comprendieron los principios básicos del lenguaje y su diferencia respecto al paradigma imperativo.  

El análisis de la aplicación TODO permitió observar cómo Haskell puede emplearse para desarrollar programas funcionales estructurados, destacando su claridad, seguridad y eficiencia en el manejo del código.

