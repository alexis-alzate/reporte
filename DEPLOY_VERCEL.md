# Despliegue en Vercel

Esta carpeta contiene solo el sitio publico del manual.

No desplegar la carpeta completa:

```text
C:\Automatizaciones\procesoAM
```

porque contiene reportes/evidencias internas.

## Carpeta correcta para desplegar

```text
C:\Automatizaciones\procesoAM\vercel-manual
```

## Opcion 1: desplegar con Vercel CLI

Abrir PowerShell y ejecutar:

```powershell
cd C:\Automatizaciones\procesoAM\vercel-manual
npx.cmd vercel login
npx.cmd vercel --prod
```

Si pregunta:

```text
Set up and deploy?
```

Responder:

```text
Y
```

Si pregunta el nombre del proyecto, usar:

```text
manual-procesos-listo
```

## Opcion 2: desplegar desde la web de Vercel

1. Entrar a:

```text
https://vercel.com/new
```

2. Crear un proyecto nuevo.
3. Subir o conectar la carpeta `vercel-manual`.
4. Framework Preset:

```text
Other
```

5. Build Command:

```text
dejar vacio
```

6. Output Directory:

```text
dejar vacio
```

7. Deploy.

## Error de token invalido

Si aparece:

```text
Error: The specified token is not valid. Use `vercel login` to generate a new token.
```

Solucion:

```powershell
cd C:\Automatizaciones\procesoAM\vercel-manual
npx.cmd vercel logout
npx.cmd vercel login
npx.cmd vercel --prod
```

El login debe hacerse con una cuenta valida de Vercel.
