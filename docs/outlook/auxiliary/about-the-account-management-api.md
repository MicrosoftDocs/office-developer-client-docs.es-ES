---
title: Información sobre la API de administración de cuentas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'La API de administración de la cuenta proporciona acceso a información de la cuenta y es compatible con las notificaciones de cambios de cuenta. Como los clientes de esta API, los proveedores de correo, haga lo siguiente:'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816051"
---
# <a name="about-the-account-management-api"></a>Información sobre la API de administración de cuentas

La API de administración de la cuenta proporciona acceso a información de la cuenta y es compatible con las notificaciones de cambios de cuenta. Como los clientes de esta API, los proveedores de correo, haga lo siguiente:
  
1. Use [IOlkAccountManager](iolkaccountmanager.md) para administrar el acceso a las cuentas y configurar las notificaciones sobre cambios de cuenta. 
    
2. Implementar y utilizar [IOlkAccountNotify](iolkaccountnotify.md) para enviar notificaciones sobre cambios de cuenta. 
    
3. Use [IOlkEnum](iolkenum.md) para enumerar las cuentas. 
    
4. Use [IOlkAccount](iolkaccount.md) para obtener y establecer propiedades y otra información acerca de una cuenta. Los clientes obtienen esta interfaz a través de [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) o [IOlkEnum::GetNext](iolkenum-getnext.md) para tener acceso a una cuenta individual. 
    
5. Implementar y utilizar [IOlkAccountHelper](iolkaccounthelper.md) para proporcionar la funcionalidad de auxiliares de cuenta Administrador, incluida la obtención de nombre de perfil de la cuenta y la sesión MAPI actual. 
    
6. Implementar y utilizar [IOlkErrorUnknown](iolkerrorunknown.md) para proporcionar información adicional sobre un error en **IOlkAccountManager**, **IOlkAccountNotify**y **IOlkAccount**. 

##  <a name="account-management-api-components"></a>Componentes de la API de administración de cuenta

La API de administración de la cuenta proporciona las siguientes definiciones, tipos de datos, interfaces, denominadas propiedades y propiedades de.
  
### <a name="definitions"></a>Definiciones
  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)
    
### <a name="data-types"></a>Tipos de datos
  
- [ACCT_BIN](acct_bin.md)
    
- [ACCT_VARIANT](acct_variant.md)
    
### <a name="interfaces"></a>Interfaces
  
- [IOlkAccount](iolkaccount.md)
    
- [IOlkAccountHelper](iolkaccounthelper.md)
    
- [IOlkAccountManager](iolkaccountmanager.md)
    
- [IOlkAccountNotify](iolkaccountnotify.md)
    
- [IOlkEnum](iolkenum.md)
    
- [IOlkErrorUnknown](iolkerrorunknown.md)
    
### <a name="named-properties"></a>Propiedades con nombre
  
- [PidLidInternetAccountName](pidlidinternetaccountname.md)
    
- [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a>Propiedades
  
- [PidTagNextSendAcct](pidtagnextsendacct.md)
    
- [PidTagPrimarySendAccount](pidtagprimarysendaccount.md)
    
- [PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md)
    
- [PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md)
    
- [PROP_ACCT_ID](prop_acct_id.md)
    
- [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)
    
- [PROP_ACCT_NAME](prop_acct_name.md)
    
- [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)
    
- [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)
    
- [PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md)
    
- [PROP_ACCT_STAMP](prop_acct_stamp.md)
    
- [PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)
    
- [PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md)
    
- [PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md)
    
- [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)
    
- [PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md)
    

