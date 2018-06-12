---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816333"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador:  <br/> |0x020A  <br/> |
|Tipo de propiedad:  <br/> |PT_DWORD  <br/> |
|Etiqueta de la propiedad:  <br/> |0x020A0003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Notas

El valor puede ser una de las siguientes constantes. Vea [constantes (API de administración de cuenta)](constants-account-management-api.md) para sus valores. 
  
|**Constantes**|**Descripción**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |No use cualquier cifrado.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Usar el cifrado de capa de sockets seguros (SSL).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Usar el protocolo de autenticación y el cifrado de seguridad de capa de transporte (TLS).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Automáticamente detectar y usar el método de cifrado compatible con el servidor de correo.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Descargas de mensaje administración de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

