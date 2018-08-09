---
title: Desarrollar DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- archivos DLL [excel 2007], crear, crear archivos DLL [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815546"
---
# <a name="developing-dlls"></a>Desarrollar DLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Una biblioteca es un cuerpo de código compilado que proporciona la funcionalidad y los datos a una aplicación ejecutable. Bibliotecas pueden ser vinculadas estáticamente o dinámicamente vinculadas y convencional tienen el lib de extensiones de nombre de archivo y .dll respectivamente. Bibliotecas estáticas (por ejemplo, la biblioteca de tiempo de ejecución de C) están vinculadas a la aplicación en la compilación y por lo que se convierten en parte del archivo ejecutable resultante. La aplicación carga un archivo DLL cuando es necesario, normalmente, cuando se inicia la aplicación. Un archivo DLL puede cargar y vincular dinámicamente a otro archivo DLL.
  
## <a name="benefits-of-using-dlls"></a>Ventajas del uso de archivos DLL

Los principales beneficios de DLL son los siguientes:
  
- Todas las aplicaciones pueden compartir una única copia en el disco.
    
- Archivos ejecutables de aplicaciones se conservan más pequeños.
    
- Permiten que los proyectos de desarrollo de gran tamaño dividir. Los desarrolladores de aplicaciones y DLL sólo necesitan acepta una interfaz entre sus elementos respectivos. Esta interfaz es exportada por el archivo DLL.
    
- Los programadores DLL pueden actualizar los archivos DLL: quizás para hacerlas más eficaz o para corregir un error, sin tener que actualizar todas las aplicaciones que usan, siempre que no cambie la interfaz exportada del archivo DLL.
    
Puede usar archivos DLL para agregar comandos y funciones de hoja de cálculo de Microsoft Excel.
  
## <a name="resources-for-creating-dlls"></a>Recursos para la creación de archivos DLL

Para crear un archivo DLL, se necesita lo siguiente:
  
- Un editor de código fuente.
    
- Un compilador para convertir código fuente en el código de objeto que es compatible con su hardware.
    
- Un vinculador para agregar código de bibliotecas estáticas, dónde se usa y para crear el archivo ejecutable de DLL.
    
Entornos de moderno de desarrollo integrado (IDE), como Microsoft Visual Studio, proporcionan todas estas cosas. También proporcionan mucho más información: inteligentes editores, herramientas para depurar el código, herramientas para administrar varios proyectos, los nuevos asistentes para proyectos y muchas otras herramientas importantes.
  
Puede crear archivos DLL en varios idiomas, por ejemplo, C o C++, Pascal y Visual Basic. Dado que el código de origen de la API que se proporcionan con Excel es C y C++, sólo estos dos lenguajes se consideran en esta documentación.
  
## <a name="exporting-functions-and-commands"></a>Exportación de funciones y comandos

Cuando se compila un proyecto de DLL, el compilador y el vinculador deben saber cuáles son las funciones que se exportará para que pueden que estén disponibles para la aplicación. En esta sección se describe las maneras en que esto se puede hacer.
  
Cuando los compiladores compilación el código fuente, en general, cambian los nombres de las funciones de su aspecto en el código fuente. Normalmente hacen esto agregando al principio y al final del nombre, en un proceso conocido como decoración de nombres. Debe asegurarse de que la función se exporta con un nombre que puedan reconocer a la aplicación al cargar el archivo DLL. Esto puede significar que indica el vinculador para asociar el nombre decorado con un nombre de exportación más sencillo. El nombre de exportación puede ser el nombre tal como aparecía originalmente en el código fuente, o algo más.
  
La forma en que el nombre está decorado depende del idioma y cómo se indica el compilador para que la función esté disponible, es decir, la convención de llamada. La convención de llamada entre procesos estándar de Windows utilizado por archivos DLL se conoce como la convención de WinAPI. Se define en archivos de encabezado de Windows como **WINAPI**, lo que a su vez se define mediante el declarador de Win32 **__stdcall**.
  
Una función de exportación de DLL para su uso con Excel (si es una función de hoja de cálculo, la hoja de macros equivalente de la función o el comando definido por el usuario) debe utilizar siempre el **WINAPI** / convención de llamada **__stdcall** . Es necesario incluir el especificador **WINAPI** explícitamente en la definición de la función como el valor predeterminado en Win32 compiladores consiste en usar la **__cdecl** convención de llamada, que también se define como **WINAPIV**, si no se especifica ninguno.
  
Puede saber el vinculador que es una función que se va a exportar y el nombre es que es conocida por externamente en una de las siguientes maneras:
  
- Colocar la función en un archivo de definición después de la palabra clave de **exportaciones** y establecer la configuración del proyecto DLL para hacer referencia a este archivo cuando la vinculación. 
    
- Use el declarador **__declspec (dllexport)** en la definición de la función. 
    
- Use una directiva de preprocesador **#pragma** para enviar un mensaje al vinculador. 
    
Aunque el proyecto puede usar los tres métodos y el compilador y el vinculador admiten, no debe intentar exportar una función de más de una de estas formas. Por ejemplo, supongamos que un archivo DLL contiene módulos de código de origen de dos, uno C y uno C++, que contienen dos funciones que se va a exportar, **Mi\_C\_exportar** y **Mis\_Cpp\_exportar** respectivamente. Por motivos de simplicidad, suponga que cada función toma un único argumento numérico de doble precisión y devuelve el mismo tipo de datos. Las alternativas para la exportación de cada función mediante el uso de cada uno de estos métodos se describen en las secciones siguientes. 
  
### <a name="using-a-def-file"></a>Uso de un archivo de definición

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

El archivo de definición, a continuación, tendría que contienen estas líneas.
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

La sintaxis general de una línea que sigue a una instrucción **exportaciones** es como se indica a continuación. 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

Tenga en cuenta que la función C se ha decorado, pero el archivo DEF fuerza explícitamente el vinculador para exponer la función con el nombre de código de origen original (en este ejemplo). El vinculador implícitamente exporta la función C++ usando el nombre original del código, por lo que no es necesario incluir el nombre decorado en el archivo de definición.
  
Para llamadas de función de la API de Windows de 32 bits, la convención para la decoración de funciones compiladas C es como sigue: **nombre_de_función** se convierte en _ **nombre_de_función @** _n_ donde _n_ es el número de bytes, expresado como un valor decimal que ocupan todos los argumentos, con los bytes para cada uno de ellos se redondea hacia arriba hasta el múltiplo más cercano de cuatro. 
  
> [!NOTE]
> Todos los punteros son ancho en Win32 de cuatro bytes. El tipo de valor devuelto tiene ningún efecto en la decoración de nombres. 
  
Es posible forzar el compilador de C++ para exponer los nombres no representativos para funciones de C++ al incluir la función y los prototipos de función, dentro de un extern "C" {...} bloquear, tal como se muestra en este ejemplo. (Las llaves **{}** se omiten aquí debido a que la declaración sólo hace referencia al bloque de código de función que inmediatamente a continuación). 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

Cuando se va a colocar los prototipos de función de C en archivos de encabezado que podrían estar incluidos en archivos de origen de C o C++, debe incluir la siguiente directiva de preprocesador.
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a>Utilizando el declarador __declspec (dllexport)

La palabra clave **__declspec (dllexport)** se puede usar en la declaración de la función de la siguiente manera. 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

La palabra clave **__declspec (dllexport)** debe agregarse en el extremo izquierdo de la declaración. Las ventajas de este enfoque son que la función no es necesario que se mostrarán en un archivo de definición, y que el estado de exportación es el adecuado con la definición. 
  
Si desea evitar una función de C++ va a estar disponible con el adorno de nombre de C++, debe declarar la función de la siguiente manera.
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

El vinculador hará que la función está disponible como my_undecorated_Cpp_export, es decir, el nombre tal como aparece en el código fuente con ningún adorno.
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>Uso de una directiva de preprocesador vinculador #pragma

Versiones más recientes de Microsoft Visual Studio admiten dos macros predefinidas que, cuando se usa junto con una directiva **#pragma** , permiten indicar el vinculador para exportar la función directamente desde el código de función. Las macros están __(función)__ y __FUNCDNAME__ (tenga en cuenta el subrayado doble al final de cada) que se expanden a los nombres de función decorado y no decorado respectivamente. 
  
Por ejemplo, cuando se usa Microsoft Visual Studio, estas líneas pueden incorporarse en un archivo de encabezado comunes como se indica a continuación.
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

Si este encabezado está incluido en los archivos de origen, las funciones de dos ejemplo, a continuación, se pueden exportar como se indica a continuación.
  
Código de C:
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

Código de C++:
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

Tenga en cuenta que la directiva debe ubicarse dentro del cuerpo de la función y sólo se expande cuando ninguna de las opciones del compilador se **establece/EP** **o/p** . Esta técnica elimina la necesidad de un archivo de definición o declaración **__declspec (dllexport)** y mantiene la especificación de su estado de exportación con el código de función. 
  
## <a name="see-also"></a>Vea también

- [Obtener acceso a DLL en Excel](how-to-access-dlls-in-excel.md)
- [Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)
- [Conceptos de programación de Excel](excel-programming-concepts.md)
- [Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

