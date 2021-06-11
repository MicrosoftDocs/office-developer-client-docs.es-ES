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
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416835"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Capas de **una interfaz IStorage** en un **objeto IStream.** 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parameters

 _lpUnkIn_
  
> [in] Puntero al **objeto IUnknown** que implementa **IStream**. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) del objeto stream. Cualquiera de los siguientes valores se puede pasar en el parámetro  _lpInterface:_ NULL, IID_IStream o IID_ILockBytes. Pasar NULL en  _lpInterface_ es lo mismo que pasar IID_IStream. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se va a crear el objeto de almacenamiento con relación a la secuencia. El valor predeterminado es STGSTRM_RESET, que proporciona al objeto de almacenamiento acceso de solo lectura e inicia en la posición cero de la secuencia. Las siguientes marcas se pueden establecer en cualquier combinación, excepto como se indica:
    
STGSTRM_CREATE 
  
> Crea un nuevo objeto de almacenamiento para el objeto stream. Esta marca no se puede establecer si STGSTRM_RESET marca está establecida. 
    
STGSTRM_CURRENT 
  
> Inicia el almacenamiento en la posición actual de la secuencia. Esta marca no se puede establecer si STGSTRM_RESET marca está establecida. 
    
STGSTRM_MODIFY 
  
> Permite al proveedor de servicios de llamadas escribir en el almacenamiento devuelto. Esta marca no se puede establecer si STGSTRM_RESET marca está establecida. 
    
STGSTRM_RESET 
  
> Inicia el almacenamiento en la posición cero. Esta marca no se puede establecer si se establece otra marca. 
    
 _lppStorageOut_
  
> [salida] Puntero a un puntero al objeto **IStorage** devuelto. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes **admiten la función HrIStorageFromStream** mediante la **interfaz IStorage** para datos adjuntos. Los proveedores de almacenamiento deben implementar la **interfaz IStream.** **HrIStorageFromStream proporciona** la **interfaz IStorage** para el **objeto IStream.** Es posible pasar un **ILockBytes** o una **interfaz IStream** en  _lpUnkIn_. 
  

