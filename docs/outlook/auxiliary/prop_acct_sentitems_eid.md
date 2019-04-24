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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327590"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta. 
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0020  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x00200102  <br/> |
|Al  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).
  
La carpeta predeterminada para los elementos enviados es **elementos enviados**.
  
Esta propiedad es de sólo lectura para cuentas POP3 e IMAP. Si se intenta establecer esta propiedad para estos tipos de cuentas, devuelve **E_ACCT_NOT_FOUND**. 
  

