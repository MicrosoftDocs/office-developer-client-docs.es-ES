---
title: Función NOW (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Devuelve el valor de fecha y hora actual.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414084"
---
# <a name="now-function-visioshapesheet"></a>Función NOW (VisioShapeSheet)

Devuelve el valor de fecha y hora actual.
  
## <a name="syntax"></a>Sintaxis

NOW ( )
  
### <a name="return-value"></a>Valor devuelto

DateTime
  
## <a name="remarks"></a>Comentarios

NOW se calcula automáticamente cada minuto. 
  
## <a name="example-1"></a>Ejemplo 1

NOW( )
  
Devuelve la fecha y hora actuales, por ejemplo 27/9/2010 16:03:30.
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(NOW(),"dd MMM., aaaa hh:mm")
  
Devuelve la fecha y hora actuales en el formato especificado, por ejemplo 27 Sep., 2010 12:03.
  
## <a name="example-3"></a>Ejemplo 3

AHORA () + 2EW.
  
Devuelve la fecha y hora actuales más dos semanas, por ejemplo 11/10/10 16:03:30.
  

