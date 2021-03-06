---
title: Información sobre la API de administración de cuentas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'La API de administración de cuentas proporciona acceso a la información de la cuenta y admite notificaciones de cambios en la cuenta. Como clientes de esta API, los proveedores de correo hacen lo siguiente:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426252"
---
# <a name="about-the-account-management-api"></a>Información sobre la API de administración de cuentas

La API de administración de cuentas proporciona acceso a la información de la cuenta y admite notificaciones de cambios en la cuenta. Como clientes de esta API, los proveedores de correo hacen lo siguiente:
  
1. Use [IOlkAccountManager para](iolkaccountmanager.md) administrar el acceso a las cuentas y configurar las notificaciones sobre los cambios en la cuenta. 
    
2. Implemente y use [IOlkAccountNotify para](iolkaccountnotify.md) enviar notificaciones sobre los cambios en la cuenta. 
    
3. Use [IOlkEnum para](iolkenum.md) enumerar cuentas. 
    
4. Use [IOlkAccount para](iolkaccount.md) obtener y establecer propiedades y otra información sobre una cuenta. Los clientes obtienen esta interfaz a través [de IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) o [IOlkEnum::GetNext](iolkenum-getnext.md) para obtener acceso a una cuenta individual. 
    
5. Implemente y use [IOlkAccountHelper](iolkaccounthelper.md) para proporcionar la funcionalidad auxiliar del administrador de cuentas, incluida la obtención del nombre de perfil de una cuenta y la sesión MAPI actual. 
    
6. Implemente y [use IOlkErrorUnknown para](iolkerrorunknown.md) proporcionar información adicional sobre un error en **IOlkAccountManager**, **IOlkAccountNotify** y **IOlkAccount**. 

##  <a name="account-management-api-components"></a>Componentes de la API de administración de cuentas

La API de administración de cuentas proporciona las siguientes definiciones, tipos de datos, interfaces, propiedades con nombre y propiedades.
  
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
    

