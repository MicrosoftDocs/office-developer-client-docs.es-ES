---
title: IUnknown IMSLogon
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
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348716"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene acceso a los recursos de un objeto de inicio de sesión del almacén de mensajes.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi. h  <br/> |
|Expuesto por:  <br/> |Objetos de inicio de sesión del almacén de mensajes  <br/> |
|Implementado por:  <br/> |Proveedores de almacenamiento de mensajes  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMSLogon  <br/> |
|Tipo de puntero:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](imslogon-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se produjo en el objeto de almacén de mensajes.  <br/> |
|[Cierre de sesión](imslogon-logoff.md) <br/> |Cierra la sesión de un proveedor de almacenamiento de mensajes.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Abre un objeto Folder o Message y devuelve un puntero al objeto para proporcionar más acceso.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aconsej](imslogon-advise.md) <br/> |Registra un objeto con un proveedor de almacenamiento de mensajes para notificaciones sobre cambios en el almacén de mensajes.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Quita el registro de un objeto para notificaciones de cambios del almacén de mensajes previamente establecidos mediante una llamada al método **IMSLogon:: Advise** .  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Abre un objeto status.  <br/> |
   
## <a name="remarks"></a>Comentarios

El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacenamiento de mensajes abierto que MAPI llama directamente. Hay una correspondencia de uno a uno entre el objeto de inicio de sesión del almacén de mensajes al que llaman las llamadas MAPI y el objeto almacén de mensajes al que llaman las aplicaciones cliente; puede considerar los objetos de inicio de sesión y de almacén como un objeto que expone dos interfaces. Los dos objetos se crean y se liberan juntos.
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

