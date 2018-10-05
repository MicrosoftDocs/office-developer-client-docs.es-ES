---
title: Compatibilidad con versiones anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidad de la versión [excel 2007], compatibilidad XLL [Excel 2007], compatibilidad con versiones anteriores [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387975"
---
# <a name="backward-compatibility"></a>Compatibilidad con versiones anteriores

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En este tema se tratan problemas de compatibilidad XLL en las diferentes versiones de Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Definiciones de constantes útiles

Considere la posibilidad de incluir definiciones similares a éstos en el código del proyecto XLL y sustituir todas las instancias de números literales que se utiliza en este contexto. Esto aclarar el código que es específico de la versión y reducir la probabilidad de errores relacionados con la versión con el formato de números inocua ¿está buscando.
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a>Introducción a la versión que se está ejecutando

Debe detectar qué versión se está ejecutando mediante `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, donde `arg` es un valor numérico **XLOPER** establecido en 2 y versión es una cadena **XLOPER** que, a continuación, se puede convertir a un número entero. Para Microsoft Excel 2013, esto es 15.0. Esto se debe hacer en o desde la función [xlAutoOpen](xlautoopen.md) . A continuación, puede establecer una variable global que se informa de todos los módulos en el proyecto que se está ejecutando la versión de Excel. El código, a continuación, puede decidir si se debe llamar a la API de C mediante **Excel12** y **XLOPER12**, o mediante **Excel4** usando **XLOPER**s.
  
Se puede llamar a **XLCallVer** para detectar la versión de la API de C, pero esto no indica cuál de las versiones de 2007 antes de Excel está ejecutando. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Crear complementos que exportan interfaces duales

Considere la posibilidad de una función XLL que toma una cadena y devuelve un valor que puede ser cualquiera de los tipos de datos de la hoja de cálculo. Puede exportar una función registrada como tipo "PD" y el prototipo manera donde la cadena se pasa como una cadena de bytes de longitud contada.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Aunque esto funciona perfectamente, existen varias razones por las ¿por qué no es la interfaz ideal para su código a partir de Excel 2007:
  
- Está sujeto a las limitaciones de cadenas de bytes de la API de C y no se puede obtener acceso a las cadenas de Unicode largas admitidas iniciar en Excel 2007.
    
- Si bien, empezando en Excel 2007, Excel puede pasar y acepte s **XLOPER**, los convierte internamente a **XLOPER12,** por lo que hay una sobrecarga de conversión implícita a partir de Excel 2007 que no existe cuando se ejecuta el código en versiones anteriores de Excel.
    
- Es posible que esta función puede convertirse en subprocesos seguros, pero si se cambia la cadena de tipo a `PD$`, se produce un error en el registro en el inicio de antes de Excel 2007.
    
Por estos motivos, idealmente, empezando en Excel 2007 debe exportar una función para los usuarios que se registró como `QD%$`, suponiendo que el código es seguro y el prototipo de subprocesos como se indica a continuación.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Otro motivo por qué es posible que desee registrar una función diferente a partir de Excel 2007 es que permite que las funciones XLL puedan tomar hasta 255 argumentos, en lugar del límite de 30 de versiones anteriores.
  
Afortunadamente, puede hacer que las ventajas de ambos métodos exportando ambas versiones desde su proyecto. Puede detectar, a continuación, la versión de Excel que se está ejecutando y registra de forma condicional la función más apropiada. Para obtener más información y un ejemplo de implementación, vea [Developing complementos (XLL) en Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Este enfoque tiene las siguientes consecuencias la posibilidad de que una hoja de cálculo que se ejecuta en Excel 2003 podría mostrar resultados diferentes de la misma hoja ejecutándose a partir de Excel 2007. Por ejemplo, podría asignar una cadena Unicode en una celda de hoja de cálculo de Excel 2003 a una cadena de bytes ASCII y truncar antes de pasar a una función XLL Excel 2003. Iniciar en Excel 2007, Excel pasará una cadena Unicode no convertida a una función XLL registrada en la forma correcta. Esto puede producir un resultado diferente. Debe tener en cuenta esta posibilidad y las consecuencias para los usuarios, no sólo en la actualización. Por ejemplo, algunas funciones numéricas integradas se mejoraron entre Excel 2000 y Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Nuevas funciones de hoja de cálculo y las funciones de herramientas para análisis

Funciones de Analysis Toolpak (ATP) forman parte de Excel a partir de Excel 2007. Anteriormente, un XLL sólo puede llamar a una función ATP mediante el uso de [xlUDF](xludf.md). Iniciar en Excel 2007, las funciones de ATP deben llamarse mediante las enumeraciones de función definidas en xlcall.h. En el ejemplo de funciones definidas por el usuario de llamada desde las DLL muestra los dos métodos diferentes.
  
## <a name="see-also"></a>Vea también

- [Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
- [Novedades de la API de C para Excel](what-s-new-in-the-c-api-for-excel.md)

