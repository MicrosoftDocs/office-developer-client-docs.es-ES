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
ms.openlocfilehash: 8dbb871a234d94f8bb2e21b15ce5de6f0db0e4ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581835"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se asigna un SCODE valor devuelto desde un objeto de almacenamiento de información OLE a un tipo de HRESULT. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parámetros

 _StgSCode_
  
> [entrada] MAPI SCODE valor devuelto desde un objeto de almacenamiento de información OLE que se asignará a un valor HRESULT.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado.
    
MAPI_E_CALL_FAILED 
  
> La función no encuentra un valor coincidente.
    
## <a name="remarks"></a>Comentarios

MAPI proporciona la función **MapStorageSCode** para el uso interno de los componentes MAPI que basar sus implementaciones de mensaje en el archivo DLL de mensajes. Debido a que estos componentes abrir almacenamiento OLE ellos mismos, debe poder asignar valores de error devueltos para problemas con el almacenamiento de OLE en un valor HRESULT. 
  
Para obtener más información, vea [Almacenamiento estructurado](structured-storage-in-mapi.md). 
  

