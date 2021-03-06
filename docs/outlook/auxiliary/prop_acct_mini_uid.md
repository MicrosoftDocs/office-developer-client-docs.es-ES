---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Devuelve un identificador de cuenta que es único en Outlook perfiles.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409436"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

Devuelve un identificador de cuenta que es único en Outlook perfiles.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0003  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Etiqueta de propiedad:  <br/> |0x00030003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtener esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md). Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**. 
  
Esta propiedad es diferente de [PROP_ACCT_ID](prop_acct_id.md) ya que su valor identifica de forma única la cuenta dentro y fuera del perfil en el que se creó la cuenta, mientras que **PROP_ACCT_ID** es única solo entre todas las cuentas dentro de ese perfil en el que se creó la cuenta. Cuando un mensaje con estas propiedades se desvía a un segundo equipo con un perfil de Outlook diferente y un conjunto de cuentas **distinto,** PROP_ACCT_MINI_UID puede identificar de forma única la cuenta original en el perfil original. Sin **embargo, PROP_ACCT_ID** posiblemente entre en conflicto con una cuenta en el perfil del segundo equipo. 
  
## <a name="see-also"></a>Vea también

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

