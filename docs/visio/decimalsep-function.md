---
title: DECIMALSEP (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Devuelve la cadena separadora decimal de la configuración regional del usuario actual.
ms.openlocfilehash: 8a59e7331fd51cf5426b5e2cdd64e3c5a22334b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360308"
---
# <a name="decimalsep-function"></a>Función DECIMALSEP

Devuelve la cadena separadora decimal de la configuración regional del usuario actual.
  
## <a name="syntax"></a>Sintaxis

DECIMALSEP( )
  
## <a name="example"></a>Ejemplo

SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

