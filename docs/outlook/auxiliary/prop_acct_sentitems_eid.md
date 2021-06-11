---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431844"
---
# <a name="prop_acct_sentitems_eid"></a>PROP_ACCT_SENTITEMS_EID

Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta. 
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0020  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x00200102  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtener esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
La carpeta predeterminada para los elementos enviados es **Elementos enviados**.
  
Esta propiedad es de solo lectura para cuentas POP3 e IMAP. Al intentar establecer esta propiedad para estos tipos de cuentas, **E_ACCT_NOT_FOUND**. 
  

