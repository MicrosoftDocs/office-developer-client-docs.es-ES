---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320156"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene un puntero a un objeto de almacén de Protocolo de acceso a mensajes de Internet (IMAP) sin envolver que proporciona acceso al archivo de carpetas personales (PST) subyacente sin invocar la sincronización y descargar los elementos.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parámetros

 _ppvObject_
  
> [salida] Puntero a un [objeto de almacén IMsgStore : IMAPIProp](imsgstoreimapiprop.md) que está desencapsulado. 
    
## <a name="return-values"></a>Valores devueltos

S_OK
  
- La llamada se ha realizado correctamente y se ha devuelto un puntero a una interfaz sin envolver en  _ppvObject_.
    
## <a name="remarks"></a>Comentarios

Sin desenvolver primero un almacén IMAP, el acceso a un mensaje en el almacén puede forzar una sincronización que intente descargar todo el mensaje. El uso del almacén sin envolver permite el acceso al mensaje en su estado actual sin desencadenar una descarga.
  
Dado que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén sin envolver, después de llamar correctamente **a UnwrapNoRef**, debe llamar a [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para mantener el recuento de referencias. 
  
## <a name="see-also"></a>Consulte también



[IProxyStoreObject](iproxystoreobject.md)

