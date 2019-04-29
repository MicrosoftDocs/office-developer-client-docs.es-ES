---
title: IUnknown IMSProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412866"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a un proveedor de almacenamiento de mensajes a través de un objeto de proveedor de almacén de mensajes. Este objeto de proveedor de almacén de mensajes se devuelve al iniciar la sesión de proveedor mediante la función de punto de entrada [MSProviderInit](msproviderinit.md) del proveedor de almacenamiento de mensajes. El objeto de proveedor de almacén de mensajes lo usan principalmente las aplicaciones cliente y la cola MAPI para abrir los almacenes de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi. h  <br/> |
|Expuesto por:  <br/> |Objetos de proveedor de almacén de mensajes  <br/> |
|Implementado por:  <br/> |Proveedores de almacenamiento de mensajes  <br/> |
|Llamado por:  <br/> |MAPI y la cola MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMSProvider  <br/> |
|Tipo de puntero:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Apagado](imsprovider-shutdown.md) <br/> |Cierra un proveedor de almacenamiento de mensajes de manera ordenada.  <br/> |
|[Inicio de sesión](imsprovider-logon.md) <br/> |Registra MAPI en una instancia de un proveedor de almacenamiento de mensajes.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Registra la cola MAPI en un almacén de mensajes.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compara dos identificadores de entrada del almacén de mensajes para determinar si hacen referencia al mismo objeto Store.  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI usa un objeto de proveedor de almacén de mensajes por sesión, independientemente de cuántos almacenes de mensajes haya abierto el proveedor del almacén. Si una segunda sesión MAPI inicia sesión en cualquier tienda abierta, las llamadas MAPI **MSProviderInit** una segunda vez para crear un nuevo objeto de proveedor de almacén de mensajes para que la sesión la use. 
  
Un objeto de proveedor de almacén de mensajes debe contener lo siguiente para funcionar correctamente:
  
- Un puntero de rutina de asignación de memoria de _lpMalloc_ para su uso en todos los almacenes abiertos mediante este objeto de proveedor. 
    
- Los punteros de la rutina _lpfAllocateBuffer_, _ lpfAllocateMore _ y _lpfFreeBuffer_ a las funciones de asignación de memoria [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Una lista vinculada de todos los almacenes abiertos con este objeto de proveedor y que aún no se han cerrado.
    
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

