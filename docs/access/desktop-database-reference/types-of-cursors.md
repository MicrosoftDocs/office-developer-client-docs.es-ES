---
title: Tipos de cursores (referencia de escritorio de la base de datos de Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717576"
---
# <a name="types-of-cursors"></a><span data-ttu-id="0c531-102">Tipos de cursores</span><span class="sxs-lookup"><span data-stu-id="0c531-102">Types of cursors</span></span>


<span data-ttu-id="0c531-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c531-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c531-p101">Como regla general, una aplicación debería utilizar el cursor más sencillo que proporcione el acceso a datos requerido. Cada característica de cursor adicional más allá de lo básico (sólo avance, sólo lectura, estático, con desplazamiento, sin búfer) supone un costo en memoria de cliente, carga de red o rendimiento. En muchos casos, las opciones predeterminadas de cursor generan un cursor más complejo que el que realmente necesita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c531-p101">As a general rule, your application should use the simplest cursor that provides the required data access. Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance. In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="0c531-107">La elección del tipo de cursor depende de cómo utiliza la aplicación el conjunto de resultados y también de diversas consideraciones de diseño, como el tamaño del conjunto de resultados, el porcentaje de datos con probabilidad de ser utilizados, la susceptibilidad a cambios de datos, y requisitos de rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c531-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="0c531-108">En el caso más básico, la elección del cursor depende de si se necesita cambiar los datos o simplemente verlos:</span><span class="sxs-lookup"><span data-stu-id="0c531-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="0c531-109">Si sólo necesita desplazarse por un conjunto de resultados, pero sin cambiar los datos, utilice un cursor [de sólo avance](forward-only-cursors.md) o [estático](static-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="0c531-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="0c531-110">Si tiene un conjunto de resultados grande y sólo necesita seleccionar algunas filas, utilice un cursor con [conjunto de claves](keyset-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="0c531-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="0c531-111">Si desea sincronizar un conjunto de resultados con incorporaciones, cambios y eliminaciones recientes de todos los usuarios simultáneos, utilice un cursor [dinámico](dynamic-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="0c531-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="0c531-112">Aunque cada tipo de cursor parece distinto, tenga en cuenta que estos tipos de cursor no varían mucho más que en el resultado de características y opciones superpuestas.</span><span class="sxs-lookup"><span data-stu-id="0c531-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

