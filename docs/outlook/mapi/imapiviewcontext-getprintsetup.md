---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351128"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera la información de impresión actual.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _lppFormPrintSetup_
  
> contempla Puntero a un puntero a una estructura que contiene la información de impresión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La información de impresión se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewContext:: GetPrintSetup** para recuperar información sobre la configuración de la impresora antes de intentar imprimir el mensaje actual. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Asigne los miembros **hDevMode** y **hDevName** de la estructura [FORMPRINTSETUP](formprintsetup.md) mediante el uso de la función **GlobalAlloc**de Win32.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si espera que los miembros **hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** a la que apunta el parámetro _LppFormPrintSetup_ sean cadenas Unicode, establezca _ulFlags_ en MAPI_UNICODE. De lo contrario, **GetPrintSetup** devolverá estas cadenas en formato ANSI. 
  
Libere los miembros **hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** llamando a la función de Win32 **GlobalFree**. Libere toda la estructura **FORMPRINTSETUP** llamando a [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Vea también



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

