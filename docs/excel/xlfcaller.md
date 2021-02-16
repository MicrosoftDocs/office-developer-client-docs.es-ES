---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- Función xlfcaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405733"
---
# <a name="xlfcaller"></a>xlfCaller

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve información sobre la celda, el rango de celdas, el comando de un menú, la herramienta de una barra de herramientas u objeto que llamó al comando DLL o la función que se está ejecutando actualmente.
  
|**Código llamado desde**|**Devuelve**|
|:-----|:-----|
|DLL  <br/> |El id. de registro.  <br/> |
|Una sola celda  <br/> |Referencia de una sola celda.  <br/> |
|Una fórmula de matriz de varias celdas  <br/> |Referencia de varias celdas.  <br/> |
|Expresión de formato condicional  <br/> |Referencia a la celda a la que se aplica la condición de formato.  <br/> |
|Un menú  <br/> | Una matriz de fila única de cuatro elementos:  <br/>  Identificador de la barra.  <br/>  Posición del menú.  <br/>  Posición del submenú.  <br/>  Posición del comando.  <br/> |
|Una barra de herramientas  <br/> | Una matriz de fila única de dos elementos:  <br/>  El número de barra de herramientas de las barras de herramientas integradas o el nombre de la barra de herramientas de las barras de herramientas personalizadas.  <br/>  Posición en la barra de herramientas.  <br/> |
|Un objeto gráfico  <br/> |Identificador de objeto (nombre del objeto).  <br/> |
|Un comando asociado a un xlcOnEnter, ON. ENTRAR, captura de eventos  <br/> |Una referencia a la celda o celdas que se están escribió.  <br/> |
|Comando asociado a xlcOnDoubleclick, ON. DOUBLECLICK, captura de eventos.  <br/> |Celda en la que se hizo doble clic (no necesariamente la celda activa).  <br/> |
|Auto_Open, AutoClose, Auto_Activate o Auto_Deactivate macro  <br/> |Nombre de la hoja de llamadas.  <br/> |
|Otros métodos no enumerados  <br/> |#REF! Error  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

El valor devuelto es uno de los siguientes tipos de datos  /  **XLOPER XLOPER12:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** o **xltypeMulti**. Dado que tres de estos tipos apuntan a memoria asignada, el valor devuelto de **xlfCaller** siempre debe liberarse en una llamada a la función [xlFree](xlfree.md) cuando ya no se necesite. 
  
Para obtener más información **acerca de** /  **XLOPER12** XLOPERs, vea [Administración de memoria en Excel.](memory-management-in-excel.md)
  
## <a name="remarks"></a>Comentarios

Esta función es la única función que no es de hoja de cálculo a la que se puede llamar desde una función de hoja de cálculo DLL/XLL. Solo se puede llamar a otras funciones de información XLM desde comandos o funciones equivalentes de hoja de macros.
  
## <a name="example"></a>Ejemplo

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Esta función llama a una macro de comandos (xlcSelect) y sólo funcionará correctamente cuando se llame desde una hoja de macros.
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Consulte también



[Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

