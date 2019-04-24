---
title: Agregados descendientes del secundario
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292149"
---
# <a name="grandchild-aggregates"></a>Agregados descendientes del secundario


**Se aplica a:** Access 2013, Office 2013

A la columna de capítulo creada en una cláusula de un comando Shape se le puede asignar un *nombre de alias de capítulo* (normalmente con la palabra clave AS). Se puede identificar cualquier columna de cualquier capítulo del objeto **Recordset** con forma mediante un nombre completo que identifica al elemento secundario que contiene la columna. Por ejemplo, si el capítulo principal, cap1, contiene un capítulo secundario, cap2, que tiene una columna de cantidad, cant, el nombre completo sería cap1.cap2.cant. El nombre completo se puede usar como argumento de una de las funciones de agregado (SUMA, MEDIA, MÁX, MÍN, CONTAR, DESVEST o ANY).

