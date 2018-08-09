---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: dc802d8fef0d90672428c8bfa3662a2734637d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816199"
---
# <a name="iolkaccount"></a>IOlkAccount

Admite la obtención y definición de propiedades y otra información acerca de una cuenta.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
|Suministrado por:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) y [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Obtiene el tipo y las categorías de la cuenta especificada.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Obtiene el valor de la propiedad de cuenta especificado. Vea la siguiente tabla de propiedades.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Establece el valor de la propiedad de cuenta especificado. Vea la siguiente tabla de propiedades.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Libera memoria asignada por la interfaz **IOlkAccount** .  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admiten o documentado.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Confirma los cambios realizados en el objeto de cuenta mediante la escritura en el almacén del registro.  <br/> |
   
## <a name="properties"></a>Propiedades

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Representa el identificador de entrada de la carpeta de entrega predeterminado para la cuenta.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Devuelve el identificador de cuenta en Outlook 2000 y versiones anteriores de Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Es True si la cuenta es una cuenta de Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Devuelve el identificador de cuenta en las versiones de Outlook con respecto a Outlook 2002.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Devuelve el nombre de cuenta.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Recupera el identificador exclusivo (UID) de la sección de perfil que almacena las preferencias de cuenta.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Devuelve la marca de "Enviar" de la cuenta.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Devuelve la marca de cuenta.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Devuelve el nombre de usuario para mostrar.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Especifica la dirección de correo electrónico para la cuenta.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Representa una estructura [ACCT_BIN](acct_bin.md) que contiene el identificador exclusivo de una cuenta de Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Recupera o establece el identificador de entrada de la libreta de direcciones para la cuenta.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Representa la configuración de transporte que usa Microsoft Outlook para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de interfaz (IU) de usuario que no es compatible con la cuenta.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz es devuelto por **IOlkAccountManager::FindAccount** cuando se busca una cuenta que es compatible con **IOlkAccount** y **IOlkEnum::GetNext** al obtener la siguiente cuenta en un enumerador. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

