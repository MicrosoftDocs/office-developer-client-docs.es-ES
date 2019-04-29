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
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425879"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se produjo en el objeto de almacén de mensajes. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior para el objeto de almacén de mensajes.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene la información de versión, componente y contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si no hay ningún **MAPIERROR** para devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Use el método **IMSLogon:: GetLastError** para recuperar la información que se mostrará en un mensaje al usuario sobre el último error devuelto desde una llamada de método para el objeto de almacén de mensajes. 
  
Para liberar toda la memoria asignada por MAPI para la estructura **MAPIERROR** devuelta, las aplicaciones cliente solo deben llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
El valor devuelto de **GetLastError** debe ser S_OK para que una aplicación use **MAPIERROR**. Incluso si el valor devuelto es S_OK, es posible que no se devuelva un **MAPIERROR** . Si la implementación no puede determinar cuál era el último error o si un **MAPIERROR** no está disponible para ese error, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
## <a name="see-also"></a>Ver también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

