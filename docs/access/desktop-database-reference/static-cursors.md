---
title: Cursores estáticos (referencia de escritorio de la base de datos de Access)
TOCTitle: Static Cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f60bce47f76214d26f75d13dece5bc062fd4db61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889829"
---
# <a name="static-cursors"></a><span data-ttu-id="f2ed7-102">Cursores estáticos</span><span class="sxs-lookup"><span data-stu-id="f2ed7-102">Static Cursors</span></span>


<span data-ttu-id="f2ed7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2ed7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2ed7-p101">El cursor estático siempre muestra el conjunto de resultados tal como era cuando el cursor se abrió por primera vez. Según la implementación, los cursores estáticos pueden ser de sólo lectura o de lectura y escritura, y proporcionar desplazamiento hacia adelante y hacia atrás. El cursor estático normalmente no detecta los cambios realizados en la pertenencia, en el orden ni en los valores del conjunto de resultados tras abrir el cursor. Los cursores estáticos pueden detectar sus propias actualizaciones, eliminaciones e inserciones, aunque no se requiere que lo hagan.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-p101">The static cursor always displays the result set as it was when the cursor was first opened. Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling. The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened. Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="f2ed7-p102">Los cursores estáticos no detectan nunca las actualizaciones, eliminaciones ni inserciones del resto de las aplicaciones. Por ejemplo, suponga que un cursor estático recupera una fila y otra aplicación la actualiza. Si la aplicación vuelve a obtener la fila desde el cursor estático, los valores que ve no reflejan los cambios realizados por la otra aplicación. Se admiten todos los tipos de desplazamiento, pero los proveedores pueden o no admitir marcadores.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-p102">Static cursors never detect other updates, deletes, and inserts. For example, suppose a static cursor fetches a row, and another application then updates that row. If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application. All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="f2ed7-p103">Si la aplicación requiere desplazamientos y no necesita detectar cambios en los datos, el cursor estático es la mejor opción. Utilice **adOpenStatic** **CursorTypeEnum** para indicar que desea utilizar un cursor estático en ADO.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-p103">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice. Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

