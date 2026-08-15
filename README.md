# Mi presupuesto · Cuaderno de dinero

Cuaderno interactivo para armar un presupuesto personal o familiar. Está pensado para clase de cultura financiera y para uso doméstico: el lenguaje es claro desde los 10 años y no pide registro, cuenta ni datos personales.

**Página publicada:** https://USUARIO.github.io/mi-presupuesto/

> Cambia `USUARIO` por tu nombre de usuario de GitHub una vez que publiques.

## Qué hace

- Presupuesto **mensual**, con opción de partir el mes en **dos quincenas** o **cuatro semanas**.
- Cada ingreso y cada gasto puede **repartirse** entre las partes del mes o **asignarse a una sola**, para registrar quincenas desiguales (una quincena con bono, otra sin él) y pagos que caen todos al inicio del mes.
- Catálogo de **15 tipos de ingreso** y más de **70 gastos** en 11 categorías, con explicación breve de cada concepto. También se pueden agregar partidas propias.
- Clasificación de gastos en **fijos y variables (hormiga)** y en **vitales, importantes y prescindibles**.
- Saldo del mes, saldo por parte del mes y **saldo acumulado**, que detecta cuándo el mes cierra bien pero se rompe a mitad de camino.
- Con saldo positivo: reparto del sobrante en **ahorro, inversión y deuda** por porcentajes, con proyección y cálculo del fondo de emergencia.
- Con saldo cero o negativo: simulador de recorte que empieza por lo prescindible y sigue con lo importante.
- Gráficas de flujo, anillos de composición del gasto, barras de gastos mayores y comparación con la regla 50-30-20.
- Consejos calculados con los propios números del usuario, más un botón para pedir análisis a una IA.
- Resumen para copiar, descargar o imprimir.

## Privacidad

Todo lo que se escribe se guarda **solo en el navegador de quien usa la página** (`localStorage`). No hay servidor, ni base de datos, ni analítica, ni cookies de terceros. Nada de lo capturado sale del dispositivo, salvo el resumen que la persona decida copiar y pegar en otro lado.

## Publicar en GitHub Pages

### Opción A · desde la web, sin instalar nada

1. En GitHub, entra a **New repository**.
2. Nombre: `mi-presupuesto`. Visibilidad: **Public**. No marques ninguna casilla de inicialización.
3. Crea el repositorio y, en la pantalla siguiente, usa **uploading an existing file**.
4. Arrastra los cinco archivos de esta carpeta: `index.html`, `404.html`, `favicon.svg`, `README.md`, `LICENSE` y `.nojekyll`.
5. Escribe un mensaje como `Versión 1.2` y confirma con **Commit changes**.
6. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
7. Espera de uno a dos minutos y abre `https://USUARIO.github.io/mi-presupuesto/`.

> El archivo `.nojekyll` no se ve en el explorador de archivos de GitHub porque empieza con punto. Si no lo puedes arrastrar, créalo con **Add file → Create new file**, escribe `.nojekyll` como nombre, deja el contenido vacío y confirma.

### Opción B · desde la terminal

```bash
git init
git add .
git commit -m "Versión 1.2"
git branch -M main
git remote add origin https://github.com/USUARIO/mi-presupuesto.git
git push -u origin main
```

Después activa Pages en **Settings → Pages** con la rama `main` y la carpeta raíz.

## Actualizar la página

Sube el nuevo `index.html` encima del anterior y confirma el cambio. GitHub Pages vuelve a publicar en un par de minutos. Si no ves los cambios, recarga con `Ctrl + F5` (o `Cmd + Shift + R` en Mac): el navegador guarda copia del archivo anterior.

## Dominio propio (opcional)

Si tienes un dominio, agrega en la raíz del repositorio un archivo llamado `CNAME` con una sola línea que contenga el dominio, por ejemplo `presupuesto.ejemplo.mx`, y apunta el DNS a GitHub Pages siguiendo la [documentación oficial](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Sobre el botón de IA

El botón intenta conectarse a un servicio de inteligencia artificial. En una página estática de GitHub Pages no hay ninguno disponible, así que ofrece la salida práctica: copiar la consulta ya armada con el presupuesto y pegarla en el chat que cada quien use.

**No pongas una clave de API en este archivo.** Todo lo que se sube a un repositorio público queda a la vista, incluso si después lo borras del historial visible. Cualquiera podría usar esa clave y el consumo se te cobraría a ti. Si algún día quieres el análisis automático, hay que hacerlo con una función intermedia en un servidor, no dentro del HTML.

## Estructura

```
index.html      la aplicación completa, en un solo archivo
404.html        página de error
favicon.svg     ícono del sitio
.nojekyll       evita que GitHub procese el sitio con Jekyll
README.md       este archivo
LICENSE         licencia MIT
```

No hay dependencias que instalar ni proceso de compilación. El único recurso externo son las tipografías de Google Fonts; si no cargan, el cuaderno funciona igual con las tipografías del sistema.

## Uso en clase

El material se puede compartir, adaptar y reutilizar bajo licencia MIT, conservando el aviso de autoría. Si lo modificas para tu grupo, basta con editar `index.html`: los catálogos de ingresos y gastos están al inicio del bloque `<script>`, en los arreglos `CAT_INGRESOS` y `CAT_GASTOS`.

## Autoría

Jorge Luis Hernández Ulloa
Unidad Académica de Contaduría y Administración, Universidad Autónoma de Nayarit
ORCID: [0000-0002-5102-6011](https://orcid.org/0000-0002-5102-6011)
