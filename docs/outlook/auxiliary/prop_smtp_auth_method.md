---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica el método de autenticación que se usará para la cuenta de SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816337"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Especifica el método de autenticación que se usará para la cuenta de SMTP.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador:  <br/> |0x0208  <br/> |
|Tipo de propiedad:  <br/> |PT_DWORD  <br/> |
|Etiqueta de la propiedad:  <br/> |0x02080003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor es una máscara de bits de las siguientes constantes. Vea [constantes (API de administración de cuenta)](constants-account-management-api.md) para sus valores. 
  
- **SMTP_AUTH_SAME_AS_POP** significa que con las mismas credenciales que el servidor de correo entrante, tal y como proporcionado por [PROP_INET_USER](prop_inet_user.md) y [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** significa que con las credenciales como proporcionado por [PROP_SMTP_USER](prop_smtp_user.md) y [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** significa que solicita al usuario que inicie sesión en el servidor de correo entrante antes de enviar correo. 
    
## <a name="see-also"></a>Vea también

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

