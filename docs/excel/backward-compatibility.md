---
title: Compatibilidad con versiones anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidad de versiones [Excel 2007], compatibilidad de XLL [Excel 2007], compatibilidad con versiones anteriores [Excel 2007]
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
  
En este tema se tratan los problemas de compatibilidad de XLL en diferentes versiones de Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Definiciones de constantes útiles

Considere la posibilidad de incluir definiciones similares a estas en el código del proyecto XLL y reemplazar todas las instancias de números literales que se usan en este contexto. Esto clarificará el código que es específico de la versión y reduce la probabilidad de errores relacionados con la versión en forma de números inocuos.
  
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

Debe detectar qué versión se está ejecutando usando `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, donde `arg` es un **XLOPER** numérico establecido en 2 y version es una cadena **XLOPER** que, a continuación, se puede convertir en un entero. Para Microsoft Excel 2013, es 15,0. Debe hacer esto en la función [xlAutoOpen](xlautoopen.md) . A continuación, puede establecer una variable global que informe de todos los módulos del proyecto en el que se está ejecutando la versión de Excel. A continuación, el código puede decidir si desea llamar a la API de C mediante **Excel12** y **XLOPER12**s, o usar **Excel4** con **XLOPER**s.
  
Puede llamar a **XLCallVer** para descubrir la versión de la API de C, pero esto no indica qué versiones de las versiones anteriores a Excel 2007 está ejecutando. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Creación de complementos que exportan interfaces duales

Considere una función XLL que toma una cadena y devuelve un valor que puede ser cualquiera de los tipos de datos de la hoja de cálculo. Puede exportar una función registrada como tipo "PD" y con prototipos como se indica a continuación, donde la cadena se pasa como una cadena de bytes de longitud contada.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Aunque esto funciona perfectamente, hay varias razones por las que esta no es la interfaz ideal para el código a partir de Excel 2007:
  
- Está sujeta a las limitaciones de las cadenas de bytes de la API de C y no puede tener acceso a las cadenas Unicode largas admitidas a partir de Excel 2007.
    
- Aunque, a partir de Excel 2007, Excel puede pasar y aceptar **XLOPER**, los convierte internamente a **XLOPER12**s, por lo que hay una sobrecarga de conversión implícita a partir de Excel 2007 que no está allí cuando el código se ejecuta en versiones anteriores de Excel.
    
- Puede que esta función sea segura para la realización de subprocesos, pero si se cambia la cadena `PD$`del tipo a, se produce un error en el registro al iniciarse antes de Excel 2007.
    
Por estos motivos, idealmente, a partir de Excel 2007, debe exportar una función a los usuarios que se registraron `QD%$`como, suponiendo que el código es seguro para subprocesos y prototipos de la siguiente manera.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Otro motivo por el que es posible que desee registrar una función diferente que comienza en Excel 2007 es que permite que las funciones XLL puedan tardar hasta 255 argumentos, en lugar del límite 30 de versiones anteriores.
  
Afortunadamente, puede tener las ventajas de ambas mediante la exportación de ambas versiones desde el proyecto. A continuación, puede detectar la versión de Excel en ejecución y registrar condicionalmente la función más adecuada. Para obtener más información y una implementación de ejemplo, consulte [developIng Add-Ins (XLL) en Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Este enfoque conduce a la posibilidad de que una hoja de cálculo que se ejecute en Excel 2003 pueda mostrar resultados distintos de la misma hoja que se está iniciando en Excel 2007. Por ejemplo, Excel 2003 asignaría una cadena Unicode en una celda de la hoja de cálculo de Excel 2003 a una cadena de bytes ASCII y la truncaría antes de pasarla a una función XLL. A partir de Excel 2007, Excel pasará una cadena Unicode no convertida a una función XLL registrada de la forma correcta. Esto puede provocar un resultado diferente. Debe tener en cuenta esta posibilidad y las consecuencias para los usuarios, no solo en la actualización. Por ejemplo, algunas funciones numéricas integradas se mejoraron entre Excel 2000 y Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Nuevas funciones de hoja de cálculo y herramientas de análisis

Las funciones de herramientas de análisis (ATP) forman parte de Excel a partir de Excel 2007. Anteriormente, un XLL solo podía llamar a una función ATP mediante [xlUDF](xludf.md). A partir de Excel 2007, se debe llamar a las funciones de ATP con las enumeraciones de función definidas en xlcall. h. El ejemplo en el que se llama a funciones definidas por el usuario desde dll muestra los dos métodos diferentes.
  
## <a name="see-also"></a>Vea también

- [Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programar con la API de C en Excel](programming-with-the-c-api-in-excel.md)
- [Novedades de la API de C para Excel](what-s-new-in-the-c-api-for-excel.md)

