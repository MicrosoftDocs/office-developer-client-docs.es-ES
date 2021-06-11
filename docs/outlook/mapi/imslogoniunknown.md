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
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428882"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Accede a los recursos de un objeto de inicio de sesión del almacén de mensajes.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuesto por:  <br/> |Objetos de inicio de sesión del almacén de mensajes  <br/> |
|Implementado por:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMSLogon  <br/> |
|Tipo de puntero:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el último error que se produjo para el objeto de almacén de mensajes.  <br/> |
|[Cierre de sesión](imslogon-logoff.md) <br/> |Cierra la sesión de un proveedor de almacén de mensajes.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar acceso adicional.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aconsejar](imslogon-advise.md) <br/> |Registra un objeto con un proveedor de almacén de mensajes para recibir notificaciones sobre los cambios en el almacén de mensajes.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Quita el registro de un objeto para la notificación de cambios en el almacén de mensajes establecidos anteriormente mediante una llamada al método **IMSLogon::Advise.**  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Abre un objeto status.  <br/> |
   
## <a name="remarks"></a>Comentarios

El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacén de mensajes abierto al que MAPI llama directamente. Hay una correspondencia uno a uno entre el objeto de inicio de sesión del almacén de mensajes al que llama MAPI y el objeto de almacén de mensajes al que llaman las aplicaciones cliente; puede pensar en los objetos de inicio de sesión y almacenamiento como un objeto que expone dos interfaces. Los dos objetos se crean juntos y se liberan juntos.
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

