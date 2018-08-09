---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Devuelve un identificador que identifica de forma exclusiva una cuenta en el perfil en la que se creó la cuenta.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816320"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Devuelve un identificador que identifica de forma exclusiva una cuenta en el perfil en la que se creó la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0 x 0001  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Etiqueta de la propiedad:  <br/> |0 x 00010003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md). Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**. 
  
Esta propiedad es diferente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en que su valor es único sólo entre todas las cuentas dentro de ese perfil en el que se creó la cuenta, mientras que **propiedades\_ACCT_MINI_UID** identifica la cuenta dentro y fuera del perfil en el que se creó la cuenta. Cuando se mueve un mensaje con estas propiedades en un segundo equipo con un perfil de Outlook diferente y un conjunto diferente de cuentas, **PROP_ACCT_ID** , posiblemente, puede entrar en conflicto con una cuenta en el perfil del segundo equipo y **PROP_ACCT_MINI_UID** puede identificar de forma exclusiva la cuenta original en el perfil original. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

