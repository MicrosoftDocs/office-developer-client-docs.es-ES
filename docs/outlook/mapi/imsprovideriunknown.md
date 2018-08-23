---
title: IMSProvider IUnknown
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
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579630"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a un proveedor de almacén de mensajes a través de un objeto de proveedor de almacén de mensajes. Este objeto de proveedor de almacén de mensajes se devuelve al inicio de sesión de proveedor mediante la función de punto de entrada de [MSProviderInit](msproviderinit.md) del proveedor de almacén de mensajes. El objeto de proveedor de almacén de mensajes se usa principalmente en las aplicaciones cliente y la cola de MAPI para abrir los almacenes de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuestos por:  <br/> |Objetos de proveedor de almacén de mensajes  <br/> |
|Se implementa mediante:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |MAPI y la cola de MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMSProvider  <br/> |
|Tipo de puntero:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Apagado](imsprovider-shutdown.md) <br/> |Cierra un proveedor de almacén de mensajes de una forma ordenada.  <br/> |
|[Inicio de sesión](imsprovider-logon.md) <br/> |Registros MAPI sesión en una instancia de un proveedor de almacén de mensajes.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Inicie sesión en un almacén de mensajes en la cola de MAPI.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compara dos mensajes almacén de los identificadores de entrada para determinar si hacen referencia al mismo objeto de almacenamiento.  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI utiliza un objeto de proveedor de almacén de mensajes por sesión, independientemente de cuántos mensajes se abren los almacenes por el proveedor de almacenamiento. Si un segundo MAPI sesión inicia sesión en todos los almacenes, MAPI llama **MSProviderInit** una segunda vez para crear un nuevo objeto de proveedor de almacén de mensajes de esa sesión a usar. 
  
Un objeto de proveedor de almacén de mensajes debe contener lo siguiente para funcionar correctamente:
  
- Un _lpMalloc_ asignación de memoria rutinarias puntero para su uso por todos los almacenes que se abrieron con este objeto de proveedor. 
    
- El _lpfAllocateBuffer_, _ lpfAllocateMore _ y punteros de rutina _lpfFreeBuffer_ a las funciones de asignación de memoria [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Una lista vinculada de todos los almacenes abierto mediante el uso de este objeto de proveedor y aún no se ha cerrado.
    
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

