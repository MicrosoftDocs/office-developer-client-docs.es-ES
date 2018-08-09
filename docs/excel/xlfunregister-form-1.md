---
title: xlfUnregister (Formulario 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister (función) [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815735"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (Formulario 1)

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel. Esto equivale a llamar al **Cancelar el registro** de una hoja de macros XLM de Excel. 
  
**xlfUnregister** se puede llamar de dos formas: 
  
- Formulario 1: Anula el registro de un comando individual o una función.
    
- Formulario 2: Descarga y desactiva un XLL.
    
Se llama en el formulario 1, esta función reduce el recuento de uso de una función DLL o el comando que se registró anteriormente con **xlfRegister** o **registrar**. Si el contador de uso ya es cero, esta función no tiene ningún efecto. Cuando el recuento de uso de todas las funciones en un archivo DLL llega a cero, el archivo DLL se descargue de la memoria.
  
**xlfRegister** (Formulario número 1) también define un nombre oculto que es el argumento de texto de la función, _pxFunctionText_, y que se evalúa como a la función o el identificador de registro. del comando Cuando la anulación del registro de la función, este nombre se debe eliminar con **xlfSetName** de forma que ya no aparece el nombre de función mediante el Asistente para la función. Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parámetros

_pxRegisterId_ (**xltypeNum**)
  
El identificador de registro de la función se va a anular.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**), en caso contrario, devuelve FALSE.
  
## <a name="remarks"></a>Comentarios

El registro del que identificador de la función es devuelto por **xlfRegister** cuando la función es el primera registrado. También puede obtenerse mediante una llamada a la [función xlfRegisterId](xlfregisterid.md) o la [función xlfEvaluate](xlfevaluate.md). Tenga en cuenta que xlfRegisterId intenta registrar la función si todavía no se ha registrado. Por este motivo, si sólo está intentando obtener el identificador de modo que puede anular el registro de la función, es mejor obtener pasando el nombre registrado para **xlfEvaluate**. ¿Si la función no se ha registrado, se produce un error en la **xlfEvaluate** con una #NAME? error. 
  
## <a name="example"></a>Ejemplo

Vea el código para la función **fExit** en `\SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>Vea también

- [xlfRegister (Formulario 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formulario 2)](xlfunregister-form-2.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

