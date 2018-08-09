---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817863"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Hace referencia a**: Outlook 
  
Devuelve un identificador que representa el servidor de formulario que puede administrar el formulario. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Parámetros

 _lpClassID_
  
> [entrada, salida] Un puntero para el identificador de clase (CLSID) del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de clase se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IPersistMessge::GetClassID** establece el contenido del parámetro _lpClassID_ al identificador de clase del servidor de formulario y devuelve S_OK. Cuando llama a un visor de formulario **GetClassID** y devuelve correctamente, el formulario se coloca en el estado de [Uninitialized](uninitialized-state.md) . 
  
Para obtener más información acerca de cómo se usan los identificadores de clase con objetos de almacenamiento estructurado, consulte la documentación para el método [IPersist:: GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

