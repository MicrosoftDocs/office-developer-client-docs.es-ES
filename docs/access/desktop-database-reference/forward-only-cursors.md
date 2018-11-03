---
title: Cursores de sólo avance
TOCTitle: Forward-only cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742e3a6903faf7ab817b79675b100d026e25885
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946765"
---
# <a name="forward-only-cursors"></a>Cursores de sólo avance

**Se aplica a**: Access 2013, Office 2013

El tipo de cursor predeterminado típico, denominado cursor de sólo avance (o no desplazable), sólo puede avanzar por el conjunto de resultados. Un cursor de sólo avance no admite el desplazamiento (la posibilidad de moverse hacia adelante y hacia atrás por el conjunto de resultados); sólo admite la recuperación de filas desde el principio hacia el final del conjunto de resultados. Con algunos cursores de sólo avance (como con la biblioteca de cursores de SQL Server), todas las instrucciones de inserción, actualización y eliminación creadas por el usuario activo (o confirmadas por otros usuarios) que afectan a filas del conjunto de resultados van haciéndose visibles a medida que se recuperan las filas. Sin embargo, dado que el cursor no se puede desplazar hacia atrás, los cambios realizados en filas de la base de datos ya recuperadas no son visibles a través del cursor.

Una vez procesados los datos correspondientes a la fila activa, el cursor de sólo avance libera los recursos que se utilizaron para contener los datos. Los cursores de sólo avance son dinámicos de forma predeterminada, lo que significa que todos los cambios se detectan en cuanto se procesa la fila activa. Esto permite una más rápida apertura del cursor y que el conjunto de resultados pueda mostrar actualizaciones realizadas en las tablas subyacentes.

Aunque los cursores de sólo avance no admiten el desplazamiento hacia atrás, la aplicación puede volver al principio del conjunto de resultados cerrando y volviendo a abrir el cursor. Este es un modo eficaz de trabajar con cantidades pequeñas de datos. Otra posibilidad es que la aplicación lea el conjunto de resultados una vez, almacene los datos en caché localmente y, a continuación, explore la caché de datos local.

Si la aplicación no requiere el desplazamiento por el conjunto de resultados, el cursor de sólo avance es la mejor forma de recuperar datos rápidamente con la menor cantidad de sobrecarga. Utilice el valor **adOpenForwardOnly** de **CursorTypeEnum** para indicar que desea utilizar un cursor de sólo avance en ADO.

