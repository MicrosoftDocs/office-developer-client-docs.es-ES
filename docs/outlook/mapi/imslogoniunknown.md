---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563943"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recursos de accesos en un mensaje almacenan el objeto de inicio de sesión.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuestos por:  <br/> |Objetos de inicio de sesión del almacén de mensajes  <br/> |
|Se implementa mediante:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMSLogon  <br/> |
|Tipo de puntero:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para el objeto de almacén de mensajes.  <br/> |
|[Cierre de sesión](imslogon-logoff.md) <br/> |Proveedor de almacén de registros de un mensaje.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Se abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar más acceso.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aviso](imslogon-advise.md) <br/> |Registra un objeto con un proveedor de almacén de mensajes para las notificaciones sobre cambios en el almacén de mensajes.  <br/> |
|[Desaconsejar](imslogon-unadvise.md) <br/> |Quita el registro de un objeto de notificación de cambios del almacén de mensajes ha establecido previamente mediante una llamada al método **IMSLogon::Advise** .  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Abre un objeto de estado.  <br/> |
   
## <a name="remarks"></a>Comentarios

El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacén de abrir el mensaje MAPI llama directamente. Hay una correspondencia uno a uno entre el objeto de inicio de sesión del almacén de mensajes que las llamadas MAPI y el mensaje de almacenan objetos que llaman a las aplicaciones cliente; Puede pensar en el inicio de sesión y almacenar objetos como un objeto que expone dos interfaces. Los dos objetos se crean juntos y liberado juntos.
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

