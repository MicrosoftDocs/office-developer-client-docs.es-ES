---
title: IUnknown IMAPISession
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
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328290"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra objetos asociados con una sesión de inicio de sesión MAPI.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix. h  <br/> |
|Expuesto por:  <br/> |Objetos de sesión  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISession  <br/> |
|Tipo de puntero:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](imapisession-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de sesión anterior.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Proporciona acceso a la tabla de almacén de mensajes que contiene información acerca de todos los almacenes de mensajes del perfil de sesión.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para obtener más acceso.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Abre la libreta de direcciones MAPI integrada y devuelve un puntero [IAddrBook](iaddrbookimapiprop.md) para obtener más acceso.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Proporciona acceso a la tabla de estado, una tabla que contiene información sobre todos los recursos MAPI de la sesión.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Abre un objeto y devuelve un puntero de interfaz para obtener más acceso.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aconsej](imapisession-advise.md) <br/> |Se registra para recibir una notificación de eventos especificados que afectan a la sesión.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Cancela el envío de notificaciones previamente configurado con una llamada al método adVise **** .  <br/> |
|**MessageOptions** <br/> | *No es compatible o documentado.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *No es compatible o documentado.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |En desuso. Devuelve los tipos de direcciones que pueden controlar todos los proveedores de transporte de la sesión.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Devuelve el identificador de entrada del objeto que proporciona la identidad principal para la sesión.  <br/> |
|[Cierre de sesión](imapisession-logoff.md) <br/> |Finaliza una sesión MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Devuelve un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Muestra un formulario.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Crea un token numérico que el método **ShowForm** usa para obtener acceso a un mensaje.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

