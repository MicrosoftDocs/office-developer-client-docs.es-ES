---
title: Propiedad Recordset2. UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309110"
---
# <a name="recordset2updateoptions-property-dao"></a>Propiedad Recordset2. UpdateOptions (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . OpcionesDeActualización

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Comentarios

Cuando se ejecuta **[Update](recordset2-update-method-dao.md)** en modo por lotes, DAO y la biblioteca de cursores por lotes cliente crean una serie de instrucciones SQL UPDATE para realizar los cambios necesarios. Se crea una cláusula SQL WHERE para cada actualización para aislar los registros marcados como modificados por la propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)**. Como algunos servidores remotos usan desencadenadores u otras formas para aplicar la integridad referencial, con frecuencia es importante limitar la actualización de los campos solo a los afectados por el cambio. 

Para ello, establezca la propiedad **UpdateOptions** en una de las siguientes constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** o **dbCriteriaTimeStamp**. De esta forma, solo se ejecuta la cantidad mínima total de código desencadenador. Como resultado, la operación de actualización se ejecuta con más rapidez y con menos errores potenciales.

También puede concatenar cualquiera de las constantes **dbCriteriaDeleteInsert** o **dbCriteriaUpdate** para determinar si debe utilizar un conjunto de instrucciones SQL DELETE e INSERT o una instrucción SQL UPDATE para cada actualización cuando se devuelven modificaciones por lotes al servidor. En el primer caso, se requieren dos operaciones distintas para actualizar el registro. En algunos casos, sobre todo cuando el sistema remoto implementa los desencadenadores DELETE, INSERT y UPDATE, al elegir el valor correcto de la propiedad **UpdateOptions** se puede afectar significativamente en el rendimiento.

Si no especifica ninguna de las constantes, se utilizarán **dbCriteriaUpdate** y **dbCriteriaKey**.

Los últimos registros agregados generarán siempre instrucciones INSERT y los elementos eliminados generarán instrucciones DELETE, por ello esta propiedad sólo se aplica según se modificaron los registros con las actualizaciones de las bibliotecas de cursores.

