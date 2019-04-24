---
title: xlfUnregister (Formulario 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- función xlfunregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303895"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (Formulario 1)

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se puede llamar desde un comando DLL o XLL a los que ha llamado Microsoft Excel. Esto equivale a llamar **unregister** desde una hoja de macros XLM de Excel. 
  
se puede llamar a **xlfUnregister** de dos formas: 
  
- Formulario 1: anula el registro de un comando individual o una función.
    
- Formulario 2: descarga y desactiva un XLL.
    
Esta función, que se llama en el formulario 1, reduce el recuento de uso de una función o un comando DLL que se registró previamente con **xlfRegister** o **Register**. Si el recuento de uso ya es cero, esta función no tiene ningún efecto. Cuando el recuento de todas las funciones de una DLL llega a cero, el archivo DLL se descarga de la memoria.
  
**xlfRegister** (Formulario 1) también define un nombre oculto que es el argumento del texto de la función, _pxFunctionText_, y que se evalúa en el identificador de registro de la función o el comando. Al anular el registro de la función, este nombre debe eliminarse con **xlfSetName** de modo que el nombre de la función ya no aparezca en la lista del Asistente para funciones. Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parameters

_pxRegisterId_ (**xltypeNum**)
  
IDENTIFICADOR de registro de la función que se va a anular en el registro.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se ejecuta correctamente, devuelve **true** (**xltypeBool**), de lo contrario devuelve false.
  
## <a name="remarks"></a>Comentarios

**XlfRegister** devuelve el identificador de registro de la función cuando la función se registra por primera vez. También se puede obtener llamando a la [función xlfRegisterId](xlfregisterid.md) o a la [función xlfEvaluate](xlfevaluate.md). Tenga en cuenta que xlfRegisterId intenta registrar la función si aún no se ha registrado. Por este motivo, si solo intenta obtener el identificador para que pueda anular el registro de la función, es mejor obtenerlo pasando el nombre registrado a **xlfEvaluate**. Si no se ha registrado la función, **xlfEvaluate** produce un error con un #NAME? error. 
  
## <a name="example"></a>Ejemplo

Consulte el código de la función **fExit** en `\SAMPLES\GENERIC\GENERIC.C`.
  
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

