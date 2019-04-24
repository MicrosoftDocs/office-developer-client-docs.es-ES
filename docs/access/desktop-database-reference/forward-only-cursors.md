---
title: Cursores solo de reenvío
TOCTitle: Forward-only cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65eaafe805eabbac1681aa6dcd08b6b99bb056fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292296"
---
# <a name="forward-only-cursors"></a><span data-ttu-id="0900f-102">Cursores solo de reenvío</span><span class="sxs-lookup"><span data-stu-id="0900f-102">Forward-only cursors</span></span>

<span data-ttu-id="0900f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0900f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0900f-p101">El tipo de cursor predeterminado típico, denominado cursor de sólo avance (o no desplazable), sólo puede avanzar por el conjunto de resultados. Un cursor de sólo avance no admite el desplazamiento (la posibilidad de moverse hacia adelante y hacia atrás por el conjunto de resultados); sólo admite la recuperación de filas desde el principio hacia el final del conjunto de resultados. Con algunos cursores de sólo avance (como con la biblioteca de cursores de SQL Server), todas las instrucciones de inserción, actualización y eliminación creadas por el usuario activo (o confirmadas por otros usuarios) que afectan a filas del conjunto de resultados van haciéndose visibles a medida que se recuperan las filas. Sin embargo, dado que el cursor no se puede desplazar hacia atrás, los cambios realizados en filas de la base de datos ya recuperadas no son visibles a través del cursor.</span><span class="sxs-lookup"><span data-stu-id="0900f-p101">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set. A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set. With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched. Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</span></span>

<span data-ttu-id="0900f-p102">Una vez procesados los datos correspondientes a la fila activa, el cursor de sólo avance libera los recursos que se utilizaron para contener los datos. Los cursores de sólo avance son dinámicos de forma predeterminada, lo que significa que todos los cambios se detectan en cuanto se procesa la fila activa. Esto permite una más rápida apertura del cursor y que el conjunto de resultados pueda mostrar actualizaciones realizadas en las tablas subyacentes.</span><span class="sxs-lookup"><span data-stu-id="0900f-p102">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data. Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed. This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</span></span>

<span data-ttu-id="0900f-p103">Aunque los cursores de sólo avance no admiten el desplazamiento hacia atrás, la aplicación puede volver al principio del conjunto de resultados cerrando y volviendo a abrir el cursor. Este es un modo eficaz de trabajar con cantidades pequeñas de datos. Otra posibilidad es que la aplicación lea el conjunto de resultados una vez, almacene los datos en caché localmente y, a continuación, explore la caché de datos local.</span><span class="sxs-lookup"><span data-stu-id="0900f-p103">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor. This is an effective way to work with small amounts of data. As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</span></span>

<span data-ttu-id="0900f-p104">Si la aplicación no requiere el desplazamiento por el conjunto de resultados, el cursor de sólo avance es la mejor forma de recuperar datos rápidamente con la menor cantidad de sobrecarga. Utilice el valor **adOpenForwardOnly** de **CursorTypeEnum** para indicar que desea utilizar un cursor de sólo avance en ADO.</span><span class="sxs-lookup"><span data-stu-id="0900f-p104">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead. Use the **adOpenForwardOnly** **CursorTypeEnum** to indicate that you want to use a forward-only cursor in ADO.</span></span>

