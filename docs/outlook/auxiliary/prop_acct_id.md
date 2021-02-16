---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Devuelve un identificador que identifica de forma única una cuenta dentro del perfil en el que se crea la cuenta.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407168"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

Devuelve un identificador que identifica de forma única una cuenta dentro del perfil en el que se crea la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0001  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Etiqueta de propiedad:  <br/> |0x00010003  <br/> |
|Acceso:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md). Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**. 
  
Esta propiedad es diferente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en que su valor es único solo entre todas las cuentas dentro de ese perfil en el que se creó la cuenta, mientras que **PROP \_ ACCT_MINI_UID** identifica de forma única la cuenta dentro y fuera del perfil en el que se creó la cuenta. Cuando un mensaje con estas propiedades se desvía a un segundo equipo con un perfil de Outlook diferente y un conjunto de cuentas diferente, **PROP_ACCT_ID** puede entrar en conflicto con una cuenta en el perfil del segundo equipo y **PROP_ACCT_MINI_UID** puede identificar de forma única la cuenta original en el perfil original. 
  
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

