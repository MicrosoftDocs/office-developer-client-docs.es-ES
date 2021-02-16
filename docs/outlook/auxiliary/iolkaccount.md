---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 007a44d13565889b4775f2d3fe9979685e1878b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425067"
---
# <a name="iolkaccount"></a>IOlkAccount

Admite la obtención y el establecimiento de propiedades y otra información sobre una cuenta.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Suministrado por:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) e [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Obtiene el tipo y las categorías de la cuenta especificada.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Obtiene el valor de la propiedad de cuenta especificada. Consulta la tabla Propiedades a continuación.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Establece el valor de la propiedad de cuenta especificada. Consulta la tabla Propiedades a continuación.  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Libera la memoria asignada por la **interfaz IOlkAccount.**  <br/> |
| *Miembro de marcador de posición*  <br/> | *No se admite ni se documenta.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Confirma los cambios realizados en el objeto de cuenta escribiendo en el almacén del Registro.  <br/> |
   
## <a name="properties"></a>Propiedades

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Representa el identificador de entrada de la carpeta de entrega predeterminada de la cuenta.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Representa el identificador de entrada del almacén de entrega predeterminado de la cuenta.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Devuelve el identificador de cuenta en Outlook 2000 y versiones anteriores de Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True si la cuenta es una cuenta de Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Devuelve el identificador de cuenta en versiones de Outlook desde Outlook 2002.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Devuelve el nombre de la cuenta.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Recupera el identificador único (UID) de la sección de perfil que almacena las preferencias de la cuenta.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Devuelve la marca de "envío" de la cuenta.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Devuelve la marca de cuenta.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Devuelve el nombre para mostrar del usuario.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Especifica la dirección de correo electrónico de la cuenta.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Representa una [ACCT_BIN](acct_bin.md) que contiene el UID de una cuenta de Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Recupera o establece el identificador de entrada de la libreta de direcciones de la cuenta.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Representa la configuración de transporte que Microsoft Outlook usa para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de la interfaz de usuario (UI) que la cuenta no admite.  <br/> |
   
## <a name="remarks"></a>Comentarios

**IOlkAccountManager::FindAccount** devuelve esta interfaz al buscar una cuenta compatible con **IOlkAccount** e **IOlkEnum::GetNext** al obtener la siguiente cuenta en un enumerador. 
  
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

