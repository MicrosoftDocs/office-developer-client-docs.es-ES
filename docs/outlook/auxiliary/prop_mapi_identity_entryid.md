---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Recupera o establece el identificador de entrada de la libreta de direcciones de la cuenta.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326435"
---
# <a name="prop_mapi_identity_entryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Recupera o establece el identificador de entrada de la libreta de direcciones de la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2002  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x20020102  <br/> |
|Acceso:  <br/> |Lectura/escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

 **PROP \_ No \_ se espera que MAPI IDENTITY \_ ENTRYID** exista en todas las cuentas. Por ejemplo, una cuenta de Exchange podría tener establecido **PROP \_ MAPI IDENTITY \_ \_ ENTRYID** y no [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), mientras que para una cuenta SMTP/POP3 se invierte la situación. **PROP \_ MAPI_IDENTITY_ENTRYID** devuelve un identificador de entrada similar al valor devuelto por  _lppEntryID_ en [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)

