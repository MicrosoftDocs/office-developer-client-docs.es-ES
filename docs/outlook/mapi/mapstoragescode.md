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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416527"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un valor devuelto de SCODE de un objeto de almacenamiento OLE a un tipo HRESULT. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parámetros

 _StgSCode_
  
> [entrada] MAPI SCODE devuelve el valor de un objeto de almacenamiento OLE que se asignará a un valor HRESULT.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor esperado.
    
MAPI_E_CALL_FAILED 
  
> La función no puede encontrar un valor que coincida.
    
## <a name="remarks"></a>Comentarios

MAPI proporciona la **función MapStorageSCode** para el uso interno de componentes MAPI que basan sus implementaciones de mensajes en la DLL del mensaje. Dado que estos componentes abren el almacenamiento OLE por sí mismos, deben ser capaces de asignar valores de error devueltos para problemas con el almacenamiento OLE a un valor HRESULT. 
  
Para obtener más información, vea [Almacenamiento estructurado.](structured-storage-in-mapi.md) 
  

