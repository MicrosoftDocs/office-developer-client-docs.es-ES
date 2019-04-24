---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- función xlfCaller [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310230"
---
# <a name="xlfcaller"></a>xlfCaller

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve información sobre la celda, el rango de celdas, el comando de un menú, la herramienta de una barra de herramientas o el objeto que llamó a la función o al comando DLL que se está ejecutando actualmente.
  
|**Código llamado desde**|**Devuelve**|
|:-----|:-----|
|Biblioteca  <br/> |IDENTIFICADOR del registro.  <br/> |
|Una sola celda  <br/> |Una referencia de una sola celda.  <br/> |
|Una fórmula de matriz de varias celdas  <br/> |Una referencia de varias celdas.  <br/> |
|Una expresión de formato condicional  <br/> |Referencia a la celda a la que se aplica la condición de formato.  <br/> |
|Un menú  <br/> | Una matriz de una sola fila de cuatro elementos:  <br/>  IDENTIFICADOR de la barra.  <br/>  La posición del menú.  <br/>  Posición del submenú.  <br/>  Posición del comando.  <br/> |
|Una barra de herramientas  <br/> | Una matriz de una sola fila de dos elementos:  <br/>  El número de la barra de herramientas para las barras de herramientas integradas o el nombre de la barra de herramientas de las barras de herramientas personalizadas.  <br/>  Posición de la barra de herramientas.  <br/> |
|Un objeto gráfico  <br/> |Identificador de objeto (nombre de objeto).  <br/> |
|Comando asociado a un xlcOnEnter, ON. ENTRAR, captura de eventos  <br/> |Referencia a la celda o celdas que se van a especificar.  <br/> |
|Comando asociado a un xlcOnDoubleclick, ON. DOUBLECLICK, captura de eventos.  <br/> |La celda en la que se hizo doble clic (no necesariamente la celda activa).  <br/> |
|Auto_Open, autoCierre, Auto_activar o Auto_desactivar macro  <br/> |Nombre de la hoja de llamada.  <br/> |
|Otros métodos no incluidos  <br/> |#REF! Error  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

El valor devuelto es uno de los siguientes tipos de datos **XLOPER**/ **XLOPER12** : **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**o **xltypeMulti**. Dado que tres de estos tipos apuntan a la memoria asignada, el valor devuelto de **xlfCaller** siempre debe liberarse en una llamada a la [función xlFree](xlfree.md) cuando ya no es necesaria. 
  
Para obtener más información acerca de **XLOPER**/ **xloper12** consulte [Administración de memoria en Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Comentarios

Esta función es la única función que no es de hoja de cálculo a la que se puede llamar desde una función de hoja de cálculo XLL o DLL. Otras funciones de información XLM solo pueden llamarse desde comandos o desde funciones equivalentes de hoja de macros.
  
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

