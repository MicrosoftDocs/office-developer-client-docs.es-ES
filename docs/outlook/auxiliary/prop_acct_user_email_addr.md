---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica la dirección de correo electrónico de la cuenta.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436779"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Especifica la dirección de correo electrónico de la cuenta.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000C  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Etiqueta de propiedad:  <br/> |0x000C001F  <br/> |
|Al  <br/> |Lectura y escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

 **PROP_ACCT_USER_EMAIL_ADDR** no se espera que exista en cada cuenta. Por ejemplo, una cuenta de Exchange podría tener [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) pero no **PROP_ACCT_USER_EMAIL_ADDR**, mientras que para una cuenta SMTP/POP3, la situación se invierte.
  
## <a name="see-also"></a>Ver también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)

