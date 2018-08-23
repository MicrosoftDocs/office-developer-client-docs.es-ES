---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 163bce38d665a8566fd703420ff1f7b2f44f7c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571811"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra los objetos asociados a una sesión de inicio de sesión MAPI.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Expuestos por:  <br/> |Objetos de sesión  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISession  <br/> |
|Tipo de puntero:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de la sesión anterior.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Proporciona acceso a la tabla de almacenamiento de mensaje que contiene información acerca de todos los almacenes de mensaje en el perfil de sesión.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Se abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para aún más el acceso.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Se abre la libreta de direcciones integrada de MAPI, la devolución de un puntero [IAddrBook](iaddrbookimapiprop.md) para aún más el acceso.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Proporciona acceso a la tabla de estado, una tabla que contiene información acerca de todos los recursos MAPI en la sesión.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Se abre un objeto y devuelve un puntero de interfaz para aún más el acceso.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aviso](imapisession-advise.md) <br/> |Se registra para recibir notificaciones de los eventos que afectan a la sesión.  <br/> |
|[Desaconsejar](imapisession-unadvise.md) <br/> |Cancela el envío de notificaciones configuradas previamente con una llamada al método **Advise** .  <br/> |
|**Opciones de mensaje** <br/> | *No se admiten o documentado.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *No se admiten o documentado.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |En desuso. Devuelve los tipos de direcciones que se pueden controlar por todos los proveedores de transporte en la sesión.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Devuelve el identificador de entrada del objeto que proporciona la identidad principal para la sesión.  <br/> |
|[Cierre de sesión](imapisession-logoff.md) <br/> |Termina una sesión MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Devuelve un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Muestra un formulario.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Crea un token numérico que usa el método **ShowForm** para tener acceso a un mensaje.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

