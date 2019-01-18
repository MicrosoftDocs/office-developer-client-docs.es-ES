---
title: Cursores dinámicos (referencia de escritorio de la base de datos de Access)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726032"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="9c378-102">Cursores dinámicos</span><span class="sxs-lookup"><span data-stu-id="9c378-102">Dynamic cursors</span></span>


<span data-ttu-id="9c378-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c378-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c378-p101">Los cursores dinámicos detectan todos los cambios realizados en las filas del conjunto de resultados, independientemente de que los cambios se produzcan desde dentro del cursor o los realicen otros usuarios ajenos al cursor. Todas las instrucciones para inserción, actualización y eliminación realizadas por todos los usuarios se pueden ver a través del cursor. El cursor dinámico puede detectar cualquier cambio realizado en las filas, en el orden y en los valores del conjunto de resultados después de abrirse el cursor. Las actualizaciones realizadas fuera del cursor no son visibles hasta que se confirman (a menos que el nivel de aislamiento de la transacción del cursor esté establecido en "no guardados").</span><span class="sxs-lookup"><span data-stu-id="9c378-p101">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor. All insert, update, and delete statements made by all users are visible through the cursor. The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened. Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="9c378-p102">Por ejemplo, suponga que un cursor dinámico recupera dos filas y otra aplicación y que, a continuación, actualiza una de esas filas y elimina la otra. Si, luego, el cursor dinámico recupera esas filas, no encontrará la fila eliminada pero mostrará los valores nuevos de la fila actualizada.</span><span class="sxs-lookup"><span data-stu-id="9c378-p102">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other. If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="9c378-p103">El cursor dinámico es una buena elección si una aplicación debe detectar todas las actualizaciones simultáneas realizadas por otros usuarios. Utilice el valor **adOpenDynamic** de **CursorTypeEnum** para indicar que desea utilizar un cursor dinámico en ADO.</span><span class="sxs-lookup"><span data-stu-id="9c378-p103">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users. Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="9c378-112">[Cursores de sólo avance](forward-only-cursors.md) | [Cursores estáticos](static-cursors.md) | [Cursores con conjunto de claves](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="9c378-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

