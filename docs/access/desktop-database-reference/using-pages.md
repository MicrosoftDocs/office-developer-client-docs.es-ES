---
title: Uso de páginas (referencia de escritorio de la base de datos de Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ff4c0368d2811767b3211a664a42dfc8aac16ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874772"
---
# <a name="using-pages"></a><span data-ttu-id="66554-102">Uso de páginas</span><span class="sxs-lookup"><span data-stu-id="66554-102">Using Pages</span></span>


<span data-ttu-id="66554-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66554-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66554-104">Utilice la propiedad **NúmeroDePáginas (PageCount)** para determinar cuántas páginas de datos hay en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="66554-104">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="66554-105">*Las páginas* son grupos de registros cuyo tamaño es igual que el valor de la propiedad **PageSize** .</span><span class="sxs-lookup"><span data-stu-id="66554-105">*Pages* are groups of records whose size equals the **PageSize** property setting.</span></span> <span data-ttu-id="66554-106">Incluso aunque la última página esté incompleta porque haya menos registros que el valor de **PageSize**, cuenta como una página más en el valor **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="66554-106">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="66554-107">Si el objeto **Recordset** no admite esta propiedad, **PageCount** será -1, que significa que **PageCount** no se puede determinar.</span><span class="sxs-lookup"><span data-stu-id="66554-107">If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="66554-p102">Utilice la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad **AbsolutePage** para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor Web cuando se desea permitir al usuario que se desplace por los datos de las páginas para ver un número determinado de registros a la vez.</span><span class="sxs-lookup"><span data-stu-id="66554-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page. This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="66554-111">Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="66554-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="66554-p103">Utilice la propiedad **AbsolutePage** para identificar el número de página en el que se encuentra el registro activo. De nuevo, el proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.</span><span class="sxs-lookup"><span data-stu-id="66554-p103">Use the **AbsolutePage** property to identify the page number on which the current record is located. Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="66554-p104">**AbsolutePage** es de base uno y es igual a 1 cuando el registro activo es el primero del **conjunto de registros**. Configure esta propiedad para desplazarse al primer registro de una página determinada. Obtenga el número total de páginas a partir de la propiedad **NúmeroDePáginas (PageCount)**.</span><span class="sxs-lookup"><span data-stu-id="66554-p104">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

