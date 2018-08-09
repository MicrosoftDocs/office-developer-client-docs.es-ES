---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Devuelve un identificador de cuenta que es exclusivo a través de los perfiles de Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816321"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Devuelve un identificador de cuenta que es exclusivo a través de los perfiles de Outlook.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0003  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Etiqueta de la propiedad:  <br/> |0x00030003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md). Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**. 
  
Esta propiedad es diferente de [PROP_ACCT_ID](prop_acct_id.md) en que su valor identifica la cuenta dentro y fuera del perfil en el que se creó la cuenta, mientras que **PROP_ACCT_ID** es único sólo entre todas las cuentas dentro de ese uno perfil en el que se creó la cuenta. Cuando un mensaje con estas propiedades se desplaza hasta un segundo equipo con un perfil de Outlook diferente y un conjunto diferente de las cuentas de, **PROP_ACCT_MINI_UID** puede identificar de forma exclusiva la cuenta original en el perfil original. Sin embargo, **PROP_ACCT_ID** , posiblemente, pueden entrar en conflicto con una cuenta en el perfil del segundo equipo. 
  
## <a name="see-also"></a>Vea también

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

