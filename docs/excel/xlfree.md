---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- función xlFree [Excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424717"
---
# <a name="xlfree"></a>xlFree

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para liberar recursos de memoria asignados por Microsoft Excel al crear el valor devuelto **XLOPER**/ **XLOPER12** en una llamada a [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)o [Excel12v](excel4v-excel12v.md). La función **xlFree** libera la memoria auxiliar y restablece el puntero a **null** , pero no destruye otras partes de la**XLOPER12**de **XLOPER**/ .
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parameters

 _px_1,..., px_n_
  
Uno o más ****/ **XLOPER12**XLOPER s que se van a liberar. En versiones de Excel de hasta 2003, el número máximo de punteros que se pueden pasar es 30. A partir de Excel 2007, se incrementa a 255.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Esta función no devuelve un valor.
  
## <a name="remarks"></a>Comentarios

Debe liberar todos los **XLOPER** que reciba como un valor devuelto desde **Excel4** o **Excel4v** y cada **XLOPER12** que se obtiene como un valor devuelto de **Excel12** o **Excel12v** si son uno de los siguientes tipos: **xltypeStr **, **XltypeMulti**o **xltypeRef**. Siempre es seguro liberar otros tipos incluso si no usan memoria auxiliar, siempre y cuando los haya obtenido de **Excel4** o **Excel12**.
  
Cuando regrese a Excel un puntero a un **XLOPER XLOPER**/ **** que aún contiene memoria asignada a Excel que se va a liberar, debe establecer **xlbitXLFree** para asegurarse de que Excel libera la memoria. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se llama a **get. ÁREA de trabajo (1)** para devolver la plataforma en la que se está ejecutando Excel actualmente como una cadena. El código copia esta cadena devuelta en un búfer para su uso posterior. El código vuelve a colocar el búfer en **XLOPER12** para su uso posterior con la función de Excel. Por último, el código muestra la cadena en un cuadro de alerta. 
  
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

