---
title: Cancel (método, RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868752"
---
# <a name="cancel-method-rds"></a>Cancel (método, RDS)


**Se aplica a**: Access 2013, Office 2013

Cancela la ejecución de una llamada de método asincrónico pendiente.

## <a name="syntax"></a>Sintaxis

*RDS*. *DataControl*. Cancelar

## <a name="remarks"></a>Comentarios

Al llamar a **Cancel**, [ReadyState](readystate-property-rds.md) se establece automáticamente en **adcReadyStateLoaded** y el objeto [Recordset](recordset-object-ado.md) estará vacío.

