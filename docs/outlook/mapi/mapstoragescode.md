---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357634"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un valor de devolución SCODE de un objeto de almacenamiento OLE a un tipo HRESULT. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parameters

 _StgSCode_
  
> a Valor devuelto MAPI SCODE de un objeto de almacenamiento OLE que se va a asignar a un valor HRESULT.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realizó correctamente y devolvió el valor esperado.
    
MAPI_E_CALL_FAILED 
  
> La función no puede encontrar un valor que coincida.
    
## <a name="remarks"></a>Comentarios

MAPI proporciona la función **MapStorageSCode** para el uso interno de componentes MAPI que basen sus implementaciones de mensajes en la dll del mensaje. Como estos componentes abren por sí mismos el almacenamiento OLE, deben poder asignar valores de error devueltos para problemas con el almacenamiento OLE en un valor HRESULT. 
  
Para obtener más información, consulte [Structured Storage](structured-storage-in-mapi.md). 
  

