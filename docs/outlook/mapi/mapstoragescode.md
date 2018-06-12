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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818301"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _StgSCode_
  
> [entrada] MAPI SCODE valor devuelto desde un objeto de almacenamiento de información OLE que se asignará a un valor HRESULT.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado.
    
MAPI_E_CALL_FAILED 
  
> La función no encuentra un valor coincidente.
    
## <a name="remarks"></a>Notas

MAPI proporciona la función **MapStorageSCode** para el uso interno de los componentes MAPI que basar sus implementaciones de mensaje en el archivo DLL de mensajes. Debido a que estos componentes abrir almacenamiento OLE ellos mismos, debe poder asignar valores de error devueltos para problemas con el almacenamiento de OLE en un valor HRESULT. 
  
Para obtener más información, vea [Almacenamiento estructurado](structured-storage-in-mapi.md). 
  

