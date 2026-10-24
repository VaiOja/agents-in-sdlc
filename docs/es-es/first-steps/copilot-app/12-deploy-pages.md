---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de cambios y comprobar el Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz con GitHub Pages para que cualquiera pueda acceder a él. Copilot puede preparar el flujo de trabajo y guiarte durante la implementación, pero sigues siendo responsable de revisar los cambios y confirmar que el sitio está publicado.

En esta lección:

- Pide a Copilot que configure la publicación con GitHub Pages.
- Revisa el flujo de trabajo y la solicitud de cambios antes de combinarla.
- Sigue la implementación y comprueba el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero quienes lo visitan aún necesitan una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo pone a disposición en una URL pública sin añadir un servidor ni una dependencia de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama en tres etapas: una solicitud de cambios de space-quiz combinada; una ejecución correcta de Deploy website en GitHub Actions, con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y combine una solicitud de cambios y que modifique la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de implementación y cualquier solicitud de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba la implementación

1. Confirma que el archivo README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios de la solicitud, incluidos los pasos de compilación e implementación del flujo de trabajo.
3. Combina la solicitud únicamente cuando hayan pasado las comprobaciones obligatorias.
4. Sigue la ejecución de implementación de GitHub Actions hasta que termine correctamente.
5. Abre la URL indicada y confirma que Space Quiz se carga.

Si el agente no puede activar Pages o combinar la solicitud, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que la implementación se complete correctamente y el sitio publicado se cargue.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio publicado y has comprobado la implementación en lugar de confiar únicamente en el informe del agente. Continúa con la [lección 13: Repaso y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
