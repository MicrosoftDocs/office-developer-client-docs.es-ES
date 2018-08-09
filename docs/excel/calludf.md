---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815515"
---
# <a name="calludf"></a>CallUDF

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función definida por el usuario en un entorno informático de alto rendimiento.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parámetros

_SessionId_
  
> El identificador de la sesión en el que se va a realizar la llamada.
    
_XLLName_
  
> El nombre del XLL que contiene la función definida por el usuario.
    
_UDFName_
  
> El nombre de la función definida por el usuario.
    
_CallBackAddr_
  
> La función que el conector debe llamar cuando se completa la función definida por el usuario.
    
_pxAsyncHandle_
  
> El identificador asincrónico utilizado por Excel y el conector para realizar un seguimiento de la llamada de función definida por el usuario pendiente. El conector utiliza más adelante cuando finalice la llamada, cuando llama a Excel mediante el puntero de función se pasa en el argumento _CallBackAddr_ . 
    
_ArgCount_
  
> El número de argumentos que se pasan a la función definida por el usuario. El valor máximo permitido es de 255.
    
_Parámetro1_
  
> Un valor que se pase a la función definida por el usuario. Repita este argumento para cada parámetro indicado por _ArgCount_.
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si la llamada UDF se inicia correctamente; **xlHpcRetInvalidSessionId** si el argumento de _SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores, incluidos el tiempo de espera. Si la llamada devuelve cualquier código de error (nada excepto **xlHpcRetSuccess**), a continuación, Excel considera la llamada UDF al que se ha producido un error, invalida la _pxAsyncHandle_y no espera a que se produzca una devolución de llamada.
  
## <a name="remarks"></a>Comentarios

Esta función se ejecuta de forma asincrónica.
  
## <a name="see-also"></a>Vea también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

