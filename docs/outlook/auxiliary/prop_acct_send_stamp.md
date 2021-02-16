---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Devuelve el accountsendstamp.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423009"
---
# <a name="prop_acct_send_stamp"></a>PROP_ACCT_SEND_STAMP

Devuelve la marca de "envío" de la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000E  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Etiqueta de propiedad:  <br/> |0x000E001F  <br/> |
|Acceso:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md). Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

