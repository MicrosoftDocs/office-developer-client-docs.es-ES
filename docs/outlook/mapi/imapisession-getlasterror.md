---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435582"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error de sesión anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Identificador del valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, componente y contexto del error. El _parámetro lppMAPIError_ se puede establecer en NULL si MAPI no puede proporcionar la información adecuada para una **estructura MAPIERROR.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se MAPI_UNICODE marca y la sesión no admite Unicode.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::GetLastError** recupera información sobre el último error devuelto por una llamada al método **IMAPISession.** Los clientes pueden proporcionar a sus usuarios información detallada sobre el error si incluyen esta información en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR,** si MAPI proporciona una, a la que apunta el parámetro  _lppMAPIError_ solo si **GetLastError** devuelve S_OK. A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, **GetLastError** devuelve un puntero a NULL  _en lppMAPIError_ en su lugar. 
  
Para obtener más información acerca **del método GetLastError,** vea [Errores extendidos de MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Consulte también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Errores extendidos de MAPI](mapi-extended-errors.md)

