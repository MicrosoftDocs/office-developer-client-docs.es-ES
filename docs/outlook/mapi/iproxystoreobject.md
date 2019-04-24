---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315522"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona un objeto de almacén del Protocolo de acceso a mensajes de Internet (IMAP) que se ha Desempaquetado y que permite el acceso a los elementos del archivo de carpetas personales (PST) sin invocar la sincronización y descargar los elementos.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Heredado de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Proporcionado por:  <br/> |Proveedor de almacenamiento de mensajes  <br/> |
|Identificador de interfaz:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
| *Marcador de posición de miembro*  <br/> | *No es compatible o documentado.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Obtiene un puntero a un almacén IMAP desencapsulado.  <br/> |
| *Marcador de posición de miembro*  <br/> | *No es compatible o documentado.*  <br/> |
   
## <a name="remarks"></a>Comentarios

Llame a [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en el almacén de mensajes de origen para obtener la interfaz **IProxyStoreObject** . A continuación, llame a **IProxyStoreObject:: UnwrapNoRef** para obtener el objeto de almacén desempaquetado. Si **QueryInterface** devuelve el error **MAPI_E_INTERFACE_NOT_SUPPORTED**, entonces el almacén no se ha ajustado. 
  
Dado que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén desencapsulado, después de llamar a **UnwrapNoRef**correctamente, debe llamar a [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para mantener el recuento de referencia. 
  

