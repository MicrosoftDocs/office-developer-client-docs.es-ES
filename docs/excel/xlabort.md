---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- función xlAbort [Excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310258"
---
# <a name="xlabort"></a>xlAbort

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Cede el procesador a otras tareas del sistema y comprueba si el usuario ha presionado la **tecla ESC** para cancelar una macro. Si el usuario ha presionado la **tecla ESC** durante la actualización de un libro, también se puede detectar desde dentro de una función de hoja de cálculo llamando a esta función. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Parameters

 _pxRetain_ (**xltypeBool**)
  
(Opcional). Si **es false**, esta función comprueba la condición break y borra cualquier interrupción pendiente. Esto permite al usuario continuar a pesar de la condición de interrupción. Si se omite este argumento o es **true**, la función comprueba si el usuario se ha anulado sin borrarlo.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve **true** (**xltypeBool**) si el usuario ha presionado la **tecla ESC**.
  
## <a name="remarks"></a>Comentarios

### 

#### <a name="frequent-calls-may-be-needed"></a>Las llamadas frecuentes pueden ser necesarias

Las funciones y los comandos que pueden tardar mucho tiempo deben llamar a esta función con frecuencia para que el procesador se entregue a otras tareas del sistema.
  
#### <a name="avoid-sensitive-language"></a>Evitar el idioma confidencial

Evite usar el término "anular" en la interfaz de usuario. Considere la posibilidad de usar "Cancelar", "detener", "interrumpir" o "detener" en su lugar.
  
## <a name="example"></a>Ejemplo

El código siguiente mueve repetidamente la celda activa en una hoja hasta que haya transcurrido un minuto o hasta que el usuario presione la **tecla ESC**. Llama a la función **xlAbort** de vez en cuando. Esto produce el procesador, con lo que se facilita la multitarea cooperativa. 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a>Vea también



[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

