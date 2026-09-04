# Control Horas Mundo Natura

PWA estática para registrar jornadas de mañana y tarde, con almacenamiento local por mes, cálculo de objetivos y horas extra, e informes mensuales exportables a PDF.

## Publicación en GitHub Pages

El proyecto ya contiene el flujo automático de publicación en [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml). Sigue estos pasos una única vez:

1. En [GitHub](https://github.com/new), crea un repositorio nuevo llamado `control-horas-mundo-natura`. Selecciona **Public** o **Private** según prefieras y no añadas archivos iniciales.
2. En el Mac, abre Terminal dentro de esta carpeta y ejecuta los siguientes comandos, sustituyendo `TU_USUARIO` por tu nombre de usuario de GitHub:

   ```bash
   git init
   git add .
   git commit -m "Primera versión de Control Horas Mundo Natura"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/control-horas-mundo-natura.git
   git push -u origin main
   ```

3. En el repositorio de GitHub, abre **Settings → Pages**. En “Build and deployment”, selecciona **GitHub Actions** como fuente.
4. Espera a que finalice la acción “Publicar PWA en GitHub Pages”. La dirección pública quedará disponible en **Settings → Pages**, normalmente como `https://TU_USUARIO.github.io/control-horas-mundo-natura/`.

En futuras actualizaciones solo tendrás que ejecutar:

```bash
git add .
git commit -m "Describe el cambio realizado"
git push
```

## Ejecutar en Mac

Desde esta carpeta, inicia un servidor estático:

```bash
ruby -run -e httpd . -p 8080
```

Después abre [http://localhost:8080](http://localhost:8080) en Safari. Los datos se guardan en el almacenamiento local de ese navegador, por lo que no se pierden al recargar ni al cerrar Safari.

## Instalar en iPhone

Cuando GitHub Pages esté publicado, abre su dirección HTTPS desde Safari en el iPhone y toca **Compartir → Añadir a pantalla de inicio**. Se instalará con su icono propio y estará disponible a pantalla completa.

El navegador guarda los datos localmente en cada dispositivo: no se sincronizan entre el Mac y el iPhone en esta primera versión.

## Exportar el informe

El botón **Exportar a PDF** abre el informe preparado para imprimir. En Safari para Mac selecciona **PDF → Guardar como PDF**; en iPhone usa el panel de compartir de la vista de impresión para guardarlo o enviarlo.
