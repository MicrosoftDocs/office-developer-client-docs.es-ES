---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- función xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815738"
---
# <a name="xlfree"></a>xlFree

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para liberar memoria recursos asignados por Microsoft Excel al crear la devolución de valor **XLOPER**/ **XLOPER12** en una llamada a [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)o [Excel12v](excel4v-excel12v.md). La función **xlFree** libera la memoria auxiliar y restablece el puntero en **NULL** , pero no destruye otras partes de la **XLOPER**/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Sintaxis

 _px_1,..., px_n_
  
Uno o más **XLOPER**/ s**XLOPER12**liberarse. En las versiones de Excel hasta 2003, el número máximo de punteros que se pueden pasar es 30. Iniciar en Excel 2007, se aumenta a 255.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

Esta función no devuelve un valor.
  
## <a name="remarks"></a>Notas

Debe liberar cada **XLOPER** que se obtiene como un valor devuelto de **Excel4** o **Excel4v** y cada **XLOPER12** que se obtiene como valor devuelto desde **Excel12** o **Excel12v** si son uno de los siguientes tipos: xltypeStr ** **, **xltypeMulti**o **xltypeRef**. Siempre es seguro libre a otros tipos incluso si no usan memoria auxiliar, siempre que obtuvo de **Excel4** o **Excel12**.
  
Donde se va a devolver a Excel un puntero a un **XLOPER**/ **XLOPER12** que aún contiene memoria asignada de Excel que se va a liberar, debe establecer el **xlbitXLFree** para garantizar la memoria de versiones de Excel. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se llama **obtener. WORKSPACE(1)** para devolver la plataforma en que Excel se está ejecutando como una cadena. El código copia este valor devuelto de cadena en un búfer para usarlo más adelante. El código coloca el búfer de copia en el **XLOPER12** para usarlo más adelante con la función de Excel. Por último, el código muestra la cadena en un cuadro de alerta. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Ver también

- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

