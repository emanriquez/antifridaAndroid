#U - DETECT FRIDA

## Comenzando 馃殌

Estas instrucciones te permitir谩n obtener una copia del proyecto en funcionamiento en tu m谩quina local para prop贸sitos de desarrollo y pruebas.

Mira **Deployment** para conocer como desplegar el proyecto.

Que hace este proyecto?

- Detectar a trav茅s de canalizaciones con nombre utilizadas por Frida
- Detectar a trav茅s de un hilo con nombre espec铆fico de frida
- Compare la secci贸n de texto en la memoria con la secci贸n de texto en el disco tanto para libc como para la biblioteca nativa

Adem谩s, este proyecto tiene 3 mecanismos para endurecer el c贸digo nativo.

1.  Reemplazar ciertas llamadas libc con syscalls
2.  Reemplazar cadena, operaci贸n relacionada con la memoria con implementaci贸n personalizada
3.  Aplicar la ofuscaci贸n nativa de O-LLVM

### Pre-requisitos 馃搵

Android Studio

## Despliegue 馃摝

1. Clonar Repositorio
2. Copiar carpeta app/src/main/c en su proyecto Android.
3. Agregar en app/build.gradle llamados a Librerias Nativas Cmake

麓
cmake {
path "src/main/c/CMakeLists.txt"
version "3.10.2"
}
麓 4. En MainApplication agregar llamdo a Librerias Nativas

// Used to load the 'native-lib' library on application startup.
static {
System.loadLibrary("native-lib");
}

5. Compile Aplicaci贸n en Android y Acepte nuevos componentes.

## Contribute

Elias Manriquez <eamanriquez@gmail.com>

## Autores

https://github.com/darvincisec/DetectFrida

## Licencia 馃搫

Este proyecto est谩 bajo la Licencia (CC) - mira el archivo [LICENSE.md](LICENSE.md) para detalles
