---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica la dirección de correo electrónico para la cuenta.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816325"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Especifica la dirección de correo electrónico para la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000C  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Etiqueta de la propiedad:  <br/> |0x000C001F  <br/> |
|Access:  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="remarks"></a>Notas

 **PROP_ACCT_USER_EMAIL_ADDR** no se espera que existen en cada cuenta. Por ejemplo, podría tener una cuenta de Exchange [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) pero no **PROP_ACCT_USER_EMAIL_ADDR**, mientras que para una cuenta POP3/SMTP, la situación se invierte.
  
## <a name="see-also"></a>Ver también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)

