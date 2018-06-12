---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Devuelve el accountsendstamp.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816311"
---
# <a name="propacctsendstamp"></a>PROP_ACCT_SEND_STAMP

Devuelve la marca de "Enviar" de la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000E  <br/> |
|Tipo de propiedad:  <br/> |PT_UNICODE  <br/> |
|Etiqueta de la propiedad:  <br/> |0x000E001F  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Notas

Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md). Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Ver también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

