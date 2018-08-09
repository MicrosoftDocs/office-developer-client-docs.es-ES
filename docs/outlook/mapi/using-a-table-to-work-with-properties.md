---
title: Usar una tabla para trabajar con propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820943"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="b3975-103">Usar una tabla para trabajar con propiedades</span><span class="sxs-lookup"><span data-stu-id="b3975-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="b3975-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3975-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3975-105">Muchas propiedades están disponibles desde los objetos que los admiten tanto como columnas en las tablas.</span><span class="sxs-lookup"><span data-stu-id="b3975-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="b3975-106">Siempre que sea posible, recuperar estas propiedades a través de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b3975-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="b3975-107">Llamar a [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas las propiedades que necesita el cliente y [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b3975-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="b3975-108">Estos dos llamadas normalmente son suficientes para recuperar la información suficiente para mostrar a un usuario y con frecuencia suficientes para cualquier procesamiento interno necesario, realizar una llamada a **OpenEntry** para abrir el objeto innecesario.</span><span class="sxs-lookup"><span data-stu-id="b3975-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="b3975-109">Hay sólo dos excepciones:</span><span class="sxs-lookup"><span data-stu-id="b3975-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="b3975-110">Si la propiedad es más de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="b3975-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="b3975-111">El ** IMAPITable ** interfaz no puede devolver el valor de propiedad completa, en su lugar el truncamiento a 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="b3975-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="b3975-112">Piense en este equilibrio, aunque.</span><span class="sxs-lookup"><span data-stu-id="b3975-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="b3975-113">Si va a mostrar estos datos al usuario, 255 bytes puede ser suficiente para un campo de texto, como un comentario.</span><span class="sxs-lookup"><span data-stu-id="b3975-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="b3975-114">Si necesita una propiedad concreta de una sola fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="b3975-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="b3975-115">En este caso no es necesario crear una tabla con las propiedades que nunca se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b3975-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="b3975-116">La mayor parte del tiempo, necesitará las mismas propiedades para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="b3975-116">Most of the time you will need the same properties for all rows.</span></span>
    

