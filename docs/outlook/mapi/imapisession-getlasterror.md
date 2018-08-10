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
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817435"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Hace referencia a**: Outlook 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de la sesión anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un identificador para el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si MAPI no puede proporcionar la información adecuada para una estructura **MAPIERROR** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la sesión no es compatible con Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::GetLastError** recupera información sobre el último error que se ha devuelto por una llamada al método **IMAPISession** . Los clientes pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de esta información en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** , si MAPI proporciona uno, indicada por el sólo de si de parámetro _lppMAPIError_ **GetLastError** devuelve S_OK. En ocasiones, MAPI no puede determinar cuál era el último error o no tiene nada más para informar sobre el error. En esta situación, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MAPI extendida de errores](mapi-extended-errors.md)

