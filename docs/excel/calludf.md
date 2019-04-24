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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304168"
---
# <a name="calludf"></a>CallUDF

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función definida por el usuario en un entorno informático de alto rendimiento.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parameters

_SessionId_
  
> IDENTIFICADOR de la sesión en la que se va a realizar la llamada.
    
_XLLName_
  
> El nombre del XLL que contiene la función definida por el usuario.
    
_UDFName_
  
> Nombre de la función definida por el usuario.
    
_CallBackAddr_
  
> La función a la que debe llamar el conector cuando finaliza la función definida por el usuario.
    
_pxAsyncHandle_
  
> El identificador asincrónico usado por Excel y el conector para realizar un seguimiento de la llamada pendiente a la función definida por el usuario. El conector lo usa más adelante cuando finaliza la llamada, cuando vuelve a llamar a Excel con el puntero de función pasado en el argumento _CallBackAddr_ . 
    
_ArgCount_
  
> Número de argumentos que se van a pasar a la función definida por el usuario. El valor máximo permitido es 255.
    
_Parameter1_
  
> Valor que se va a pasar a la función definida por el usuario. Repita este argumento para cada parámetro indicado por _ArgCount_.
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si la llamada a la UDF se inicia correctamente; **xlHpcRetInvalidSessionId** si el argumento _SessionID_ no es válido; **xlHpcRetCallFailed** en otros errores, incluido el tiempo de espera. Si la llamada devuelve un código de error (cualquier cosa excepto **xlHpcRetSuccess**), Excel considera que la llamada a UDF no ha podido realizarse, invalida el _pxAsyncHandle_y no espera que se produzca una devolución de llamada.
  
## <a name="remarks"></a>Comentarios

Esta función se ejecuta de forma asincrónica.
  
## <a name="see-also"></a>Vea también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

