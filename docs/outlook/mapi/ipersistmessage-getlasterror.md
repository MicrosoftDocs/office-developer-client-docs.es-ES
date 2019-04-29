---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426712"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la estructura [MAPIERROR](mapierror.md) devueltas en el parámetro _lppMAPIError_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si el formulario no puede proporcionar información adecuada para una estructura **MAPIERROR** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y el proveedor de la libreta de direcciones no admite Unicode, o no se estableció MAPI_UNICODE y el proveedor de la libreta de direcciones solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario implementan el método **IPersistMessage:: GetLastError** para proporcionar información sobre una llamada a un método anterior que no se ha realizado correctamente. Los visores de formularios pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura [MAPIERROR](mapierror.md) en un cuadro de diálogo. 
  
Una llamada a **GetLastError** no afecta al estado del formulario. Cuando **GetLastError** devuelve el formulario permanece en el estado en el que se encontraba antes de realizar la llamada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** , si el formulario proporciona uno, al que apunta el parámetro _LppMAPIError_ solo si **GetLastError** Devuelve S_OK. A veces el formulario no puede determinar el último error o no tiene nada más para informar sobre el error. En esta situación, el formulario devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Ver también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

