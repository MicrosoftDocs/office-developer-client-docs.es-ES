---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Representa una estructura ACCT_BIN que contiene el UID de una cuenta de Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326554"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Representa una estructura [ACCT_BIN](acct_bin.md) que contiene el UID de una cuenta de Exchange. 
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2009  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x20090102  <br/> |
|Al  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).
  
Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) para comprobar si la cuenta es una cuenta de Exchange. Si es así, **prop\_MAPI_EMSMDB_UID** es un **ACCT_BIN** que contiene el **emsmdbUID**, que es el identificador único de la cuenta de Exchange. Si la cuenta no es una cuenta de Exchange, esta propiedad queda sin definir.
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)
- [Uso de varias cuentas de Exchange](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Propiedad can�nico de PidTagExchangeProfileSectionId](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

