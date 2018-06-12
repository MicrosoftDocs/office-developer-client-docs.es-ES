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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817634"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Se aplica a**: Outlook 
  
Recupera información de impresión actual.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla el tipo de las cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas devueltas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lppFormPrintSetup_
  
> [out] Puntero a un puntero a una estructura que contiene la información de impresión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La información de impresión se recuperó correctamente.
    
## <a name="remarks"></a>Notas

Objetos de formulario llamar al método **IMAPIViewContext::GetPrintSetup** para recuperar información acerca de la configuración de la impresora antes de intentar imprimir el mensaje actual. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Asignar a los miembros **hDevMode** y **hDevName** de la estructura [FORMPRINTSETUP](formprintsetup.md) mediante la función de Win32 **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si se prevé la **hDevMode** y **hDevName** miembros de la estructura **FORMPRINTSETUP** indicada por el parámetro _lppFormPrintSetup_ como cadenas Unicode, establezca _ulFlags_ en MAPI_UNICODE.. De lo contrario, **GetPrintSetup** devolverá estas cadenas en formato ANSI. 
  
Libere a los miembros **hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** mediante una llamada a la función de Win32 **GlobalFree**. Libere toda la estructura **FORMPRINTSETUP** mediante una llamada [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Ver también



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)

