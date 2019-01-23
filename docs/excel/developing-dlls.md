---
title: Desarrollar bibliotecas DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- bibliotecas dll [excel 2007], crear, crear bibliotecas DLL [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704752"
---
# <a name="developing-dlls"></a>Desarrollar bibliotecas DLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Una biblioteca es un cuerpo de código compilado que proporciona alguna funcionalidad y datos a una aplicación ejecutable. Las bibliotecas pueden estar vinculadas estáticamente o dinámicamente y tienen convencionalmente extensiones de nombre de archivo .lib y .dll respectivamente. Las bibliotecas estáticas (por ejemplo, la biblioteca en tiempo de ejecución de C) están vinculadas a la aplicación en la compilación y así se convierten en parte del ejecutable resultante. La aplicación carga una DLL cuando es necesario, normalmente, cuando se inicia la aplicación. Una DLL puede cargarse y vincularse dinámicamente con otra DLL.
  
## <a name="benefits-of-using-dlls"></a>Ventajas de usar las DLL 

Las principales ventajas de las DLL son las siguientes:
  
- Todas las aplicaciones pueden compartir una única copia en el disco.
    
- Los archivos ejecutables de las aplicaciones se mantienen más pequeños.
    
- Permiten dividir los proyectos de desarrollo de gran tamaño. Los desarrolladores de aplicaciones y DLL solo necesitan acordar una interfaz entre los elementos respectivos. La DLL exporta esta interfaz.
    
- Los desarrolladores DLL pueden actualizar las DLL, por ejemplo para que sean más eficientes o para corregir un error, sin tener que actualizar todas las aplicaciones que las usan, siempre que no cambie la interfaz de la DLL exportada.
    
Puede usar bibliotecas DLL para agregar comandos y funciones de hoja de cálculo en Microsoft Excel.
  
## <a name="resources-for-creating-dlls"></a>Recursos para crear las DLL

Para crear una DLL, necesita lo siguiente:
  
- Un editor de código fuente.
    
- Un compilador para convertir el código fuente en el código de objeto que es compatible con el hardware.
    
- Un vinculador para agregar código de bibliotecas estáticas, donde se usan, y para crear el archivo DLL ejecutable.
    
Los entornos de desarrollo integrado (IDE) modernos, como Microsoft Visual Studio, proporcionan estos elementos. También proporcionan mucho más: editores inteligentes, herramientas para depurar el código, herramientas para administrar varios proyectos, nuevos asistentes de proyectos y muchas otras herramientas importantes.
  
Puede crear bibliotecas DLL en varios lenguajes, por ejemplo, C o C++, Pascal y Visual Basic. Como el código fuente de la API proporcionado con Excel es en C y C++, se consideran solo estos dos lenguajes en esta documentación.
  
## <a name="exporting-functions-and-commands"></a>Exportar comandos y funciones

Al compilar un proyecto DLL, el compilador y vinculador necesitan saber cuáles son las funciones para exportar para que puedan estar disponibles para la aplicación. Esta sección describe las maneras para realizar esta operación.
  
Cuando los compiladores compilan el código fuente, por lo general, cambian los nombres de las funciones en el mismo. Normalmente hacen esto agregando elementos al principio o al final del nombre, en un proceso denominado decoración de nombres. Deberá asegurarse de que la función se exporta con un nombre que la aplicación que carga la DLL pueda reconocer. Esto puede significar indicarle al vinculador que asocie al nombre representativo un nombre de exportación más sencillo. El nombre de exportación puede ser el mismo nombre que aparecía originalmente en el código fuente u otro.
  
La manera de crear un nombre representativo depende del lenguaje y de cómo se indica al compilador que ponga la función a disposición, es decir, la convención de llamada. La convención de llamada entre procesos estándar para Windows que usan las DLL se conoce como la convención WinAPI. Se define en archivos de encabezado de Windows como **WINAPI**, que a su vez se define con el declarador Win32 **__stdcall**.
  
Para usar una función de exportación de DLL ( ya sea una función de hoja de cálculo, una función de hoja macro equivalente o un comando definido por el usuario) en Excel, debe usar siempre la convención de llamada **WINAPI** / **__stdcall**. Es necesario incluir el especificador **WINAPI** explícitamente en la definición de la función porque en los compiladores Win32 se usa de forma predeterminada la convención de llamada **__cdecl**, que también se define como ** WINAPIV**, si no se especifica ninguna.
  
Puede indicar al vinculador que se va a exportar una función y que el nombre se debe conocer externamente mediante uno de los siguientes métodos. Es posible:
  
- Colocar la función de un archivo DEF después de la palabra clave **EXPORTS** y establecer la configuración del proyecto DLL para que haga referencia a este archivo al realizar el vínculo. 
    
- Usar el declarador **__declspec(dllexport)** en la definición de la función. 
    
- Usar una directiva de preprocesador **#pragma** para enviar un mensaje al vinculador. 
    
Aunque el proyecto puede usar los tres métodos y su compilador y vinculador son compatibles con los tres, no debería intentar exportar una función con más de uno de estos métodos. Por ejemplo, supongamos que una DLL contiene dos módulos de código fuente, uno en C y otro en C++, que contienen dos funciones para exportar, **my\_C\_export** y **my\_Cpp\_export** respectivamente. Para simplificar, supongamos que cada función toma un único argumento numérico de doble precisión y devuelve el mismo tipo de datos. En las siguientes secciones se describen las alternativas para exportar cada función con cada uno de estos métodos. 
  
### <a name="using-a-def-file"></a>Usar un archivo DEF

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

El archivo DEF necesitaría contener estas líneas.
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

La sintaxis general de la línea que sigue a una instrucción **EXPORTS** es la siguiente. 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

Tenga en cuenta que la función C tiene un nombre representativo, pero el archivo DEF obliga explícitamente al vinculador que exponga la función con el nombre del código fuente original (en este ejemplo). El vinculador implícitamente exporta la función C++ usando el nombre de código original, por lo que no es necesario incluir el nombre representativo en el archivo DEF.
  
Para llamadas de función de la API de Windows de 32 bits, la convención para la asignación de un nombre representativo a funciones compiladas en C es la siguiente: **nombre_de_función** se convierte en _ **nombre_de_función @** _n_ donde _n_ es el número de bytes, expresado como un número decimal usado por todos los argumentos, para cada cual los bytes se redondean al múltiplo más cercano de cuatro.  
  
> [!NOTE]
> Todos los punteros son de cuatro bytes de ancho en Win32. El tipo de valor devuelto no tiene impacto en la decoración de nombres. 
  
Es posible forzar al compilador de C++ que no exponga los nombres representativos de las funciones de C++ escribiendo la función y cualquier prototipo de función dentro de un bloque "C" {...}  externo, como se muestra en el ejemplo. (Las llaves **{}** se omiten aquí porque la declaración sólo hace referencia al bloque de código de la función que sigue inmediatamente). 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

Cuando se colocan prototipos de función de C en archivos de encabezado que pueden incluirse en archivos de origen de C o C++, debe incluirse la directiva de preprocesador siguiente.
  
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

### <a name="using-the-declspecdllexport-declarator"></a>Usar el declarador __declspec(dllexport)

La palabra clave **__declspec(dllexport)** puede usarse en la declaración de la función como se describe a continuación. 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

La palabra clave **__declspec(dllexport)** debe agregarse en el extremo izquierdo de la declaración. Las ventajas de este método son que no es necesario que la función esté incluida en un archivo DEF y que el estado de exportación se encuentra con la definición. 
  
Si quiere evitar que una función C++ esté disponible con un nombre representativo de C++, debe declarar la función como se describe a continuación.
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

El vinculador pondrá a disposición la función como my_undecorated_Cpp_export, es decir, el nombre que aparece en el código fuente sin ninguna decoración.
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>Usar la directiva del vinculador del preprocesador #pragma

Versiones más recientes de Microsoft Visual Studio admiten dos macros predefinidas que, cuando se usan junto con una directiva **#pragma**, permiten indicar al vinculador que exporte la función directamente desde el código de función. Las macros son __FUNCTION__ y __FUNCDNAME__ (tenga en cuenta el subrayado doble de los extremos) que se expanden a los nombres de función no representativos y representativos respectivamente. 
  
Por ejemplo, si usa Microsoft Visual Studio, estas líneas pueden incorporarse a un archivo de encabezado común como se describe a continuación.
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

Si se incluye este encabezado en los archivos de origen, las dos funciones de ejemplo se pueden exportar como se describe a continuación.
  
Código C:
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

Código C++:
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

Tenga en cuenta que la directiva debe incluirse en el cuerpo de la función y sólo se expande si ninguna de las opciones **/EP** o **/P** está configurada. Esta técnica elimina la necesidad de un archivo DEF o una declaración **__declspec(dllexport)** y se mantiene la especificación de su estado de exportación con el código de la función. 
  
## <a name="see-also"></a>Vea también

- [Obtener acceso a las DLL en Excel](how-to-access-dlls-in-excel.md)
- [Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)
- [Conceptos de programación de Excel](excel-programming-concepts.md)
- [Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

