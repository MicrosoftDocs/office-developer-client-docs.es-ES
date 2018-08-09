---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817821"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Hace referencia a**: Outlook 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para el objeto de almacén de mensajes. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior para el objeto de almacén de mensajes.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ningún **MAPIERROR** para devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
## <a name="remarks"></a>Comentarios

Utilice el método **IMSLogon::GetLastError** para recuperar la información para mostrar en un mensaje al usuario sobre el último error devuelto desde una llamada al método para el objeto de almacén de mensajes. 
  
Para liberar toda la memoria asignada por MAPI para la estructura **MAPIERROR** devuelta, aplicaciones cliente necesitan llamar a sólo la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
El valor devuelto de **GetLastError** debe ser S_OK para una aplicación que use el **MAPIERROR**. Incluso si el valor devuelto es S_OK, que no se devuelvan un **MAPIERROR** . Si la implementación no puede determinar cuál era el último error, o si un **MAPIERROR** no está disponible para que el error, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

