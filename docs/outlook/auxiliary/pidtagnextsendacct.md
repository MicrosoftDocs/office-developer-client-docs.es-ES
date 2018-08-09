---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica la accountsendstamp secundaria para el mensaje.
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816314"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Especifica la marca "Enviar" de cuenta secundaria para el mensaje.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificador:  <br/> |0x0E29  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se aplica a un objeto de mensaje MAPI. Para un mensaje recibido, la marca "Enviar" de cuenta secundaria indica qué cuenta se debe enviar un directa o una respuesta con, si no se puede enviar la reenviar o responder con la cuenta principal. Para un mensaje saliente, la cuenta secundaria "Enviar" marca determina con qué cuenta para enviar el mensaje, si no se puede enviar el mensaje con la cuenta principal. Su valor es el valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) desde la interfaz de [IOlkAccount](iolkaccount.md) de la cuenta con la que se envía el mensaje. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)
- [Propiedades MAPI](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Propiedad canónica PidTagNextSendAcct](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

