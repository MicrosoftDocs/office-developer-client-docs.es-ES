---
title: Agregados secundarios
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947941"
---
# <a name="grandchild-aggregates"></a>Agregados secundarios


**Se aplica a**: Access 2013, Office 2013

La columna de capítulo creada en una cláusula de un comando shape se podrá dar un *nombre de alias de capítulo* (normalmente con la palabra clave AS). Se puede identificar cualquier columna de cualquier capítulo del **Recordset** con forma con un nombre completo que identifica al elemento secundario que contiene la columna. Por ejemplo, si el capítulo principal, Cap1, contiene un capítulo secundario, Cap2, tiene una columna de cantidad, importe, a continuación, el nombre completo sería Cap1.Cap2.Cant. A continuación, se puede usar el nombre completo como un argumento a una de las funciones de agregado (SUM, AVG, MAX, MIN, COUNT, STDEV o cualquiera).

