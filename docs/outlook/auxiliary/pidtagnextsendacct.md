---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica el parámetro accountsendstamp secundario para el mensaje.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327716"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Especifica la marca de "envío" de la cuenta secundaria para el mensaje.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificador:  <br/> |0x0E29  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se aplica a un objeto de mensaje MAPI. Para un mensaje recibido, la marca de "envío" de la cuenta secundaria indica con qué cuenta se debe enviar un reenvío o una respuesta, si no se puede enviar el reenvío o la respuesta con la cuenta principal. Para un mensaje saliente, la marca de "envío" de la cuenta secundaria determina con qué cuenta enviar el mensaje, si el mensaje no se puede enviar con la cuenta principal. Su valor es el [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) de la interfaz [IOlkAccount](iolkaccount.md) de la cuenta con la que se envía el mensaje. 
  
## <a name="see-also"></a>Consulte también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)
- [Propiedades MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Propiedad canónica PidTagNextSendAcct](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

