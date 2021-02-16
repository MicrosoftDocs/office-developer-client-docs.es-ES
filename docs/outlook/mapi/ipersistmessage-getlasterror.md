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
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la [estructura MAPIERROR](mapierror.md) devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a una **estructura MAPIERROR** que contiene información de versión, componente y contexto del error. El _parámetro lppMAPIError_ se puede establecer en NULL si el formulario no puede proporcionar la información adecuada para una **estructura MAPIERROR.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y el proveedor de libreta de direcciones no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de libreta de direcciones solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario implementan **el método IPersistMessage::GetLastError** para proporcionar información sobre una llamada de método anterior que ha fallado. Los visores de formularios pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura [MAPIERROR](mapierror.md) en un cuadro de diálogo. 
  
Una llamada a **GetLastError** no afecta al estado del formulario. Cuando **se devuelve GetLastError,** el formulario permanece en el estado en el que estaba antes de que se realizara la llamada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR,** si el formulario proporciona una, a la que apunta el parámetro  _lppMAPIError_ sólo si **GetLastError** devuelve S_OK. A veces, el formulario no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, el formulario devuelve un puntero a NULL  _en lppMAPIError_ en su lugar. 
  
Para obtener más información acerca **del método GetLastError,** vea [errores extendidos de MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Consulte también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

