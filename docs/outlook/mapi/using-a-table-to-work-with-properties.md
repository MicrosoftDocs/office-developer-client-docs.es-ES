---
title: Uso de una tabla para trabajar con propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439915"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="4281f-103">Uso de una tabla para trabajar con propiedades</span><span class="sxs-lookup"><span data-stu-id="4281f-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="4281f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4281f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4281f-105">Hay muchas propiedades disponibles tanto en los objetos que las admiten como en columnas en las tablas.</span><span class="sxs-lookup"><span data-stu-id="4281f-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="4281f-106">Siempre que sea posible, recupere estas propiedades a través de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4281f-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="4281f-107">Llame al [IMAPITable:: SetColumns](imapitable-setcolumns.md) para incluir todas las propiedades que necesita el cliente y el método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4281f-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="4281f-108">Estas dos llamadas suelen ser suficientes para recuperar la información suficiente para mostrar a un usuario y son con frecuencia suficientes para cualquier procesamiento interno necesario, haciendo una llamada a **OpenEntry** para abrir el objeto innecesario.</span><span class="sxs-lookup"><span data-stu-id="4281f-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="4281f-109">Solo hay dos excepciones:</span><span class="sxs-lookup"><span data-stu-id="4281f-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="4281f-110">Si la propiedad es de más de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="4281f-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="4281f-111">La interfaz \* \* IMAPITable \* \* puede que no devuelva el valor completo de la propiedad, en lugar de truncarla en 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="4281f-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="4281f-112">No obstante, piense en esta desventaja.</span><span class="sxs-lookup"><span data-stu-id="4281f-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="4281f-113">Si va a mostrar estos datos al usuario, 255 bytes pueden ser suficientes para un campo de texto, como un comentario.</span><span class="sxs-lookup"><span data-stu-id="4281f-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="4281f-114">Si necesita una propiedad específica de una sola fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="4281f-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="4281f-115">En este caso, no es necesario crear una tabla con propiedades que nunca se usarán.</span><span class="sxs-lookup"><span data-stu-id="4281f-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="4281f-116">La mayoría de las veces, necesitará las mismas propiedades para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="4281f-116">Most of the time you will need the same properties for all rows.</span></span>
    

