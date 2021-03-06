---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421287"
---
# <a name="prop_smtp_secure_connection"></a>PROP_SMTP_SECURE_CONNECTION

Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador:  <br/> |0x020A  <br/> |
|Tipo de propiedad:  <br/> |PT_DWORD  <br/> |
|Etiqueta de propiedad:  <br/> |0x020A0003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor puede ser una de las siguientes constantes. Consulta [Constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener sus valores. 
  
|**Constants**|**Descripción**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |No use ningún cifrado.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Use el cifrado de capa de socket seguro (SSL).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Use el protocolo de autenticación y cifrado de seguridad de la capa de transporte (TLS).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Detecte y use automáticamente el método de cifrado admitido por el servidor de correo.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

