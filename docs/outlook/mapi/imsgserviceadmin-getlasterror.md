---
title: IMsgServiceAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetLastError
api_type:
- COM
ms.assetid: 9e3c8d6e-74be-46a7-94ed-74a969caf165
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3c2db9284c0e014101bc3a3d2114a187d7cb3b4b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576633"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para un objeto de administración del servicio de mensajes. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un tipo de datos HRESULT que contiene el valor de error generado por la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y el objeto de administración del servicio de mensajes no es compatible con Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::GetLastError** recupera información sobre el último error que se ha devuelto por una llamada al método [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Los clientes pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de esta información en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Se puede hacer uso de la **MAPIERROR** estructura, si MAPI proporciona uno, indicada por el parámetro _lppMAPIError_ sólo si **GetLastError** devuelve S_OK. En ocasiones, MAPI no puede determinar qué era el último error o no tiene nada más para informar sobre el error. En esta situación, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
Para obtener más información acerca del método **GetLastError** , vea [Uso de errores extendido](mapi-extended-errors.md).
  
## <a name="see-also"></a>Recursos adicionales



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

