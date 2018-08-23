---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563929"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Capas una interfaz **IStorage** en un objeto **IStream** . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parámetros

 _lpUnkIn_
  
> [entrada] Puntero al objeto **IUnknown** implementar **IStream**. 
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) para el objeto stream. Cualquiera de los siguientes valores se puede pasar en el parámetro _lpInterface_ : NULL, IID_IStream o IID_ILockBytes. Pasando NULL en _lpInterface_ es el mismo que pasar IID_IStream. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla cómo es el objeto de almacenamiento que se creará con respecto a la secuencia. El valor predeterminado es STGSTRM_RESET, que proporciona el acceso de sólo lectura del objeto de almacenamiento y lo inicia en la posición cero de la secuencia. Las siguientes marcas se pueden establecer en cualquier combinación, excepto como se ha indicado:
    
STGSTRM_CREATE 
  
> Crea un nuevo objeto de almacenamiento para el objeto stream. Esta marca no se puede establecer si se establece la marca STGSTRM_RESET. 
    
STGSTRM_CURRENT 
  
> Inicia el almacenamiento en la posición actual de la secuencia. Esta marca no se puede establecer si se establece la marca STGSTRM_RESET. 
    
STGSTRM_MODIFY 
  
> Permite que el proveedor de servicios de llamada escribir en el almacenamiento devuelto. Esta marca no se puede establecer si se establece la marca STGSTRM_RESET. 
    
STGSTRM_RESET 
  
> Almacenamiento de información que comienza en la posición cero. Esta marca no se puede establecer si se establece cualquier otro marcador. 
    
 _lppStorageOut_
  
> [out] Puntero a un puntero al objeto **IStorage** devuelto. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Almacén de mensajes compatibilidad con proveedores la función **HrIStorageFromStream** mediante la interfaz **IStorage** para datos adjuntos. Los proveedores de almacén deben implementar la interfaz **IStream** . **HrIStorageFromStream** proporciona la interfaz **IStorage** para el objeto **IStream** . Es posible que se pase una **ILockBytes** o una interfaz **IStream** en _lpUnkIn_. 
  

