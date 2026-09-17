# 🌼 ¿Salimos un rato? — Invitación primaveral (plan de amistad)

Página interactiva de una sola pantalla para invitar a una amiga a salir, en plan amistad.
Tema de primavera con flores amarillas. Sin dependencias: un solo archivo HTML.

Inspirada en la idea de [gatitos-cita-programador](https://github.com/elizabthpazp/gatitos-cita-programador),
reescrita desde cero con otro flujo, otro diseño y tono de amistad.

## Cómo funciona

Seis pasos, con un tallo de progreso cuyas flores se van abriendo:

1. Portada con el ramo
2. La propuesta (con botón "déjame pensarlo" que se corre dos veces y después funciona de verdad)
3. Día: este sábado o este domingo
4. Plan: cine (con tres películas a elegir), parque, café o feria
5. Comida
6. Qué hacer después → resumen → confirmación con lluvia de flores y botón para copiar el plan

## Personalizar

En el `<script>`, al principio:

```js
const CONFIG = {
  amiga: "Belu",       // nombre de tu amiga
  yo:    "Inti",       // cómo firmás
  web3formsKey: "PEGA_AQUI_TU_ACCESS_KEY"  // ver sección de abajo
};
```

También funciona por URL, sin tocar el código:

```
index.html?para=Belu&de=Inti
```

Las opciones de cada paso son botones en el HTML con `data-valor`. Para cambiar planes,
comidas o películas, editá esos botones directamente — asegurate de que `data-valor`
coincida con el texto visible del botón, porque es lo que se usa en el resumen, en el
correo y en "copiar el plan".

## Recibir el plan por correo automáticamente

La página puede avisarte por correo apenas tu amiga confirma el plan, usando
[Web3Forms](https://web3forms.com) (gratis, sin necesidad de servidor propio):

1. Entrá a web3forms.com, poné tu correo y creá una Access Key (llega al toque, sin contraseña).
2. Pegá esa clave en `web3formsKey` dentro del `CONFIG` del archivo.
3. Probá la página vos mismo una vez: el primer envío te pide confirmar el correo con un
   botón de verificación. Después de eso, todos los envíos siguientes llegan directo.

Si dejás `web3formsKey` sin completar, la página funciona igual que antes, solo que no
manda nada — no rompe nada olvidarse este paso.

## Publicar en GitHub Pages

1. Creá un repositorio nuevo y subí el contenido de esta carpeta (`index.html` en la raíz).
2. En el repo: **Settings → Pages → Source: Deploy from a branch → `main` / `root`**.
3. En un minuto queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

El archivo `.nojekyll` está incluido para que GitHub Pages sirva todo tal cual.

## Licencia

Libre para usar y modificar.
