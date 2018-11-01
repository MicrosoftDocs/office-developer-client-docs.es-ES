---
title: Comandos parametrizados con comandos COMPUTE intermedios
TOCTitle: Parameterized Commands with Intervening COMPUTE Commands
ms:assetid: ff3724cd-040b-4b5f-bb9b-e6a38fd938c9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250311(v=office.15)
ms:contentKeyID: 48548959
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c44afce969af77696e52cea3bc194d73eb2ddd25
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877257"
---
# <a name="parameterized-commands-with-intervening-compute-commands"></a>Comandos parametrizados con comandos COMPUTE intermedios


**Se aplica a**: Access 2013, Office 2013

Una comando shape APPEND parametrizado típico tiene una cláusula que crea un objeto **Recordset** secundario con un comando de consulta y otra cláusula que crea un objeto **Recordset** secundario con un comando de consulta parameterizado, es decir, un comando que contiene un marcador de posición de parámetro (un signo de interrogación, "?" ). El objeto **Recordset** con forma resultante tiene dos niveles, en los que el elemento principal ocupa el nivel superior y el elemento secundario el nivel inferior.

La cláusula que crea el objeto **Recordset** secundario puede ser ahora un número arbitrario de comandos shape COMPUTE anidados, donde el comando más profundamente anidado contiene la consulta parametrizada. El objeto **Recordset** con forma resultante tiene varios niveles, en los que el elemento principal ocupa el nivel superior, el elemento secundario ocupa el nivel inferior, y un número arbitrario de objetos **Recordset** generados por los comandos shape COMPUTE ocupan los niveles intermedios.

El uso típico de esta característica es el de llamar a la función de agregado y las capacidades de agrupamiento de comandos shape COMPUTE para crear objetos **Recordset** intermedios con información analítica acerca del objeto **Recordset** secundario. Además, puesto que se trata de un comando shape parametrizado, cada vez que se obtiene acceso a una columna de capítulo del elemento principal, se puede recuperar un nuevo objeto **Recordset** secundario. Como los niveles intermedios se derivan del elemento secundario, éstos también se volverán a calcular.

