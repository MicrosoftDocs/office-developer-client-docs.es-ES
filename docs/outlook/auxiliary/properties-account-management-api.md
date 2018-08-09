---
title: Propiedades (API de administración de cuenta)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: En esta sección se describe las propiedades de la API de administración de cuenta.
ms.openlocfilehash: abf7422d941f581f66a118c35d2b6ff3c03e8b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816363"
---
# <a name="properties-account-management-api"></a>Propiedades (API de administración de cuenta)

En esta sección se describe las propiedades de la API de administración de cuenta.
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Se trata de la marca "Enviar" de cuenta secundaria para el mensaje.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Se trata de la marca de "Enviar" de la cuenta principal de un mensaje.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Representa el identificador de entrada de la carpeta de entrega predeterminado para la cuenta.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Devuelve un identificador que identifica de forma exclusiva una cuenta en el perfil en la que se creó la cuenta.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Es True si la cuenta es una cuenta de Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Devuelve un identificador de cuenta que es exclusivo a través de los perfiles de Outlook.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Devuelve o establece el nombre de cuenta.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Recupera el identificador exclusivo (UID) de la sección de perfil que almacena las preferencias de cuenta.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Devuelve la marca de "Enviar" de la cuenta.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Devuelve la marca de cuenta.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Especifica la dirección de correo electrónico para la cuenta.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Devuelve o establece el nombre de usuario para mostrar.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Representa la contraseña de usuario para un buzón de correo de Internet general.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Representa el número de puerto para un buzón de correo de Internet general.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Representa el nombre del servidor de un buzón de correo de Internet general.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Especifica si se debe usar capa de sockets seguros (SSL) para un buzón de correo de Internet general.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Especifica si se debe usar la autenticación de contraseña segura (SPA) para un buzón de correo de Internet general.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Representa el nombre de usuario para un buzón de correo de Internet general.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Representa una estructura [ACCT_BIN](acct_bin.md) que contiene el identificador exclusivo de una cuenta de Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Recupera o establece el identificador de entrada de la libreta de direcciones para la cuenta.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de interfaz (IU) de usuario que no es compatible con la cuenta.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Especifica el método de autenticación que se usará para la cuenta de SMTP.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Representa la contraseña de la cuenta de SMTP.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Representa el número de puerto de la cuenta de SMTP.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Representa el nombre del servidor de la cuenta de SMTP.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Especifica si se debe usar el protocolo de capa de sockets seguros (SSL) para la cuenta de SMTP.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Especifica si se debe usar la autenticación para la cuenta de SMTP.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Especifica si se debe usar la autenticación de contraseña segura (SPA) para la cuenta de SMTP.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Representa el nombre de usuario para la cuenta de SMTP.  <br/> |
   

