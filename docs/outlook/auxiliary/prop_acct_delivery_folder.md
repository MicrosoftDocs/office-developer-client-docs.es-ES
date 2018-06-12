---
title: PROP_ACCT_DELIVERY_FOLDER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a409c49b-b390-021e-2ec1-7a5932a0c8de
description: Representa el identificador de entrada de la carpeta de entrega predeterminado para la cuenta.
ms.openlocfilehash: 56b648b6a79e7497cab1980a86ca11d1c7a6aa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816328"
---
# <a name="propacctdeliveryfolder"></a>PROP_ACCT_DELIVERY_FOLDER

Representa el identificador de entrada de la carpeta de entrega predeterminado para la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0019  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de la propiedad:  <br/> |0x00190102  <br/> |
|Access:  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="remarks"></a>Notas

Obtener o establecer esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md) o [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.
  
La carpeta de entrega predeterminada es la **Bandeja de entrada**.
  
## <a name="see-also"></a>Ver también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

