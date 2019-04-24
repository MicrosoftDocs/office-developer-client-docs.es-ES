---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica el método de autenticación que se va a usar para la cuenta SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326505"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Especifica el método de autenticación que se va a usar para la cuenta SMTP.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador:  <br/> |0x0208  <br/> |
|Tipo de propiedad:  <br/> |PT_DWORD  <br/> |
|Etiqueta de propiedad:  <br/> |0x02080003  <br/> |
|Al  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor es una máscara de máscara de las siguientes constantes. Consulte [constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener sus valores. 
  
- **SMTP_AUTH_SAME_AS_POP** significa usar las mismas credenciales que mi servidor de correo entrante, tal y como lo proporciona [PROP_INET_USER](prop_inet_user.md) y [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** significa usar las credenciales proporcionadas por [PROP_SMTP_USER](prop_smtp_user.md) y [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** significa solicitar al usuario que inicie sesión en el servidor de correo entrante antes de enviar correo. 
    
## <a name="see-also"></a>Vea también

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

