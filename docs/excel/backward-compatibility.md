---
title: Compatibilidad con versiones anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidad de versiones [excel 2007], compatibilidad con XLL [Excel 2007],compatibilidad con versiones anteriores [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301683"
---
# <a name="backward-compatibility"></a>Compatibilidad con versiones anteriores

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En este tema se abordan los problemas de compatibilidad de XLL en diferentes versiones de Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Definiciones de constantes útiles

Considere la posibilidad de incluir definiciones similares a estas en el código de proyecto XLL y reemplazar todas las instancias de números literales usados en este contexto. Esto aclarará el código específico de la versión y reducirá la probabilidad de errores relacionados con la versión en forma de números de aspecto inocuo.
  
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

## <a name="getting-the-running-version"></a>Obtener la versión en ejecución

Debe detectar qué versión se está ejecutando con , donde es un XLOPER numérico establecido en 2 y version es una cadena XLOPER que, a continuación, se puede `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` `arg` coaccionar a un número entero.   Por Microsoft Excel 2013, esto es 15.0. Debe hacerlo en o desde la [función xlAutoOpen.](xlautoopen.md) A continuación, puede establecer una variable global que informe a todos los módulos del proyecto qué versión de Excel se está ejecutando. A continuación, el código puede decidir si se llama a la API de C mediante **Excel12** y **XLOPER12** s, o si se usa **Excel4** mediante **XLOPER** s.
  
Puede llamar a **XLCallVer para** detectar la versión de la API de C, pero esto no indica cuál de las versiones anteriores Excel 2007 que está ejecutando. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Creación de complementos que exportan interfaces duales

Considere una función XLL que toma una cadena y devuelve un valor que puede ser cualquiera de los tipos de datos de la hoja de cálculo. Puede exportar una función registrada como tipo "PD" y prototipo de la siguiente manera en que la cadena se pasa como una cadena de bytes de longitud contada.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Aunque funciona perfectamente bien, hay varias razones por las que esta no es la interfaz ideal para el código a partir de Excel 2007:
  
- Está sujeto a las limitaciones de las cadenas de bytes de la API de C y no puede tener acceso a las cadenas Unicode largas admitidas a partir de Excel 2007.
    
- Aunque, a partir de Excel 2007, Excel puede pasar y aceptar **XLOPER,** internamente los convierte en **XLOPER12,** por lo que hay una sobrecarga de conversión implícita a partir de Excel 2007 que no existe cuando el código se ejecuta en versiones anteriores de Excel.
    
- Puede ser que esta función se pueda hacer segura para subprocesos, pero si la cadena de tipo se cambia a , el registro no se puede iniciar antes de Excel `PD$` 2007.
    
Por estos motivos, idealmente, a partir de Excel 2007 debe exportar una función para los usuarios que se registró como , suponiendo que el código es seguro para subprocesos y prototipo de la siguiente `QD%$` manera.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Otra razón por la que es posible que desee registrar una función diferente a partir de Excel 2007 es que permite que las funciones XLL tomen hasta 255 argumentos, en lugar del límite de 30 de versiones anteriores.
  
Afortunadamente, puede tener las ventajas de ambos exportando ambas versiones desde el proyecto. A continuación, puede detectar la versión Excel y registrar condicionalmente la función más adecuada. Para obtener más información y una implementación de ejemplo, vea [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Este enfoque lleva a la posibilidad de que una hoja de cálculo que se ejecuta en Excel 2003 pueda mostrar resultados diferentes a la misma hoja que se ejecuta a partir de Excel 2007. Por ejemplo, Excel 2003 asignaría una cadena Unicode en una celda de hoja de cálculo de Excel 2003 a una cadena de bytes ASCII y la truncaría antes de pasarla a una función XLL. A partir Excel 2007, Excel pasará una cadena Unicode sin convertir a una función XLL registrada de la forma correcta. Esto podría dar lugar a un resultado diferente. Debe tener en cuenta esta posibilidad y las consecuencias para los usuarios, no solo en la actualización. Por ejemplo, algunas funciones numéricas integradas se mejoraron entre Excel 2000 y Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Nuevas funciones Worksheet y Analysis Toolpak

Las funciones de Analysis Toolpak (ATP) forman parte de Excel a partir Excel 2007. Anteriormente, un XLL solo podía llamar a una función ATP mediante [xlUDF](xludf.md). A partir Excel 2007, se debe llamar a las funciones ATP mediante las enumeraciones de funciones definidas en xlcall.h. El ejemplo de Llamar a funciones definidas por el usuario desde DLL muestra los dos métodos diferentes.
  
## <a name="see-also"></a>Vea también

- [Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
- [Novedades de la API de C para Excel](what-s-new-in-the-c-api-for-excel.md)

