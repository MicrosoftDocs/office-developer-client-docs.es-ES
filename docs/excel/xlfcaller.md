---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- función xlfCaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815723"
---
# <a name="xlfcaller"></a>xlfCaller

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve información acerca de la celda, el rango de celdas, el comando en un menú de la herramienta en una barra de herramientas o el objeto que llama el comando de la DLL o la función que se está ejecutando actualmente.
  
|**Llamar desde el código**|**Devuelve**|
|:-----|:-----|
|ARCHIVO DLL  <br/> |El identificador del registro.  <br/> |
|Una sola celda  <br/> |Una referencia de celda de un solo.  <br/> |
|Una fórmula de matriz de varias celdas  <br/> |Una referencia de varias celda.  <br/> |
|Una expresión de formato condicional  <br/> |Una referencia a la celda a la que se aplica la condición de formato.  <br/> |
|Un menú  <br/> | Una matriz de fila única cuatro elementos:  <br/>  Identificador de la barra.  <br/>  La posición del menú.  <br/>  La posición del submenú.  <br/>  La posición del comando.  <br/> |
|Una barra de herramientas  <br/> | Una matriz de fila única dos elementos:  <br/>  El número de la barra de herramientas para barras de herramientas integradas o el nombre de la barra de herramientas de barras de herramientas personalizadas.  <br/>  La posición en la barra de herramientas.  <br/> |
|Un objeto gráfico  <br/> |El identificador de objeto (nombre de objeto).  <br/> |
|Un comando asociado con un xlcOnEnter, en. Escriba, captura (evento)  <br/> |Una referencia a la celda o celdas que se escriben.  <br/> |
|Un comando asociado con un xlcOnDoubleclick, en. DOUBLECLICK, captura de eventos.  <br/> |La celda que se ha hecho doble clic (no necesariamente la celda activa).  <br/> |
|Macro Auto_abrir, AutoClose, Auto_activar o Auto_desactivar  <br/> |El nombre de la hoja de llamada.  <br/> |
|Otros métodos que no se muestran  <br/> |#REF! Error  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

El valor devuelto es uno de los siguientes **XLOPER**/ **XLOPER12** los tipos de datos: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**o **xltypeMulti**. Dado que tres de estos tipos de apuntar a memoria asignada, el valor devuelto de **xlfCaller** siempre debe liberarse en una llamada a la [función xlFree](xlfree.md) cuando ya no sea necesaria. 
  
Para obtener más información acerca de **XLOPER**/ **XLOPER12s** vea [Administración de memoria en Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Comentarios

Esta función es la función sólo que no son hojas de cálculo que se puede llamar desde una función de hoja de cálculo DLL o XLL. Otras funciones de información XLM sólo se pueden llamar desde los comandos o equivalente de hoja de macros funciones.
  
## <a name="example"></a>Ejemplo

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Esta función llama a una macro de comando (xlcSelect) y funcionará correctamente sólo cuando se llame desde una hoja de macros.
  
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

## <a name="see-also"></a>Vea también



[Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

