---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433014"
---
# <a name="calludf"></a>CallUDF

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función definida por el usuario en un entorno informático de alto rendimiento.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parámetros

_SessionId_
  
> Identificador de la sesión en la que se realiza la llamada.
    
_XLLName_
  
> Nombre del XLL que contiene la función definida por el usuario.
    
_UDFName_
  
> Nombre de la función definida por el usuario.
    
_CallBackAddr_
  
> La función a la que debe llamar el conector cuando finaliza la función definida por el usuario.
    
_pxAsyncHandle_
  
> El controlador asincrónico usado por Excel y el conector para realizar un seguimiento de la llamada de función definida por el usuario pendiente. El conector lo usa más adelante cuando finaliza la llamada, cuando vuelve a llamar a Excel mediante el puntero de función pasado en el argumento _CallBackAddr._ 
    
_ArgCount_
  
> Número de argumentos que se pasan a la función definida por el usuario. El valor máximo permitido es 255.
    
_Parámetro1_
  
> Valor que se pasa a la función definida por el usuario. Repita este argumento para cada parámetro indicado por  _ArgCount_.
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si la llamada UDF se inició correctamente; **xlHpcRetInvalidSessionId** si el  _argumento SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores, incluido el tiempo de espera. Si la llamada devuelve algún código de error (excepto **xlHpcRetSuccess**), Excel considera que se produjo un error en la llamada UDF, invalida  _pxAsyncHandle_ y no espera que se produzca una devolución de llamada.
  
## <a name="remarks"></a>Comentarios

Esta función se ejecuta asincrónicamente.
  
## <a name="see-also"></a>Consulte también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

