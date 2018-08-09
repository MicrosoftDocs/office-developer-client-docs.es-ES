---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816313"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta. 
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0 x 0020  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de la propiedad:  <br/> |0x00200102  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
La carpeta predeterminada para los elementos enviados es **Elementos enviados**.
  
Esta propiedad es de sólo lectura para las cuentas POP3 e IMAP. Si se intenta establecer esta propiedad para estos tipos de cuentas, devuelve **E_ACCT_NOT_FOUND**. 
  

