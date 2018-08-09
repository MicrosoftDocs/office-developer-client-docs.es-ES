---
title: Información sobre las restricciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816361"
---
# <a name="about-restrictions"></a><span data-ttu-id="c6cfa-103">Información sobre las restricciones</span><span class="sxs-lookup"><span data-stu-id="c6cfa-103">About Restrictions</span></span>

  
  
<span data-ttu-id="c6cfa-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6cfa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6cfa-105">Una restricción es una forma de limitar el número de filas en una vista para sólo las filas con los valores de las columnas que coincidan con criterios específicos.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="c6cfa-106">Hay muchas oportunidades diferentes para el uso de restricciones con tablas.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="c6cfa-107">Las aplicaciones de cliente pueden usar restricciones, por ejemplo, para filtrar una tabla de contenido para los mensajes enviados por una persona específica, para buscar las filas que no son compatibles con una propiedad o han establecido una propiedad en un valor específico o para buscar los destinatarios duplicados dentro de un Mensaje.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="c6cfa-108">Se usan los métodos [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: FindRow](imapitable-findrow.md) para establecer restricciones en una tabla.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="c6cfa-109">**Restringir** la restricción se aplica a la tabla sin tener que recuperar todas las filas.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="c6cfa-110">Para recuperar sólo las filas que cumplen la restricción, se requiere una llamada posterior al [IMAPITable:: QueryRows](imapitable-queryrows.md) o un método similar.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="c6cfa-111">**FindRow** se aplica la restricción y recupera la primera fila en la tabla que coincida con los criterios.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="c6cfa-112">**FindRow** se aplica una restricción temporal, que es en existencia sólo para la duración de la llamada, mientras que **Restrict** se aplica una restricción más permanente.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="c6cfa-113">Algunos clientes pueden generar una restricción de uso de columnas que no están en la columna actual conjunto.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="c6cfa-114">Compatibilidad con esta restricción es opcional y los implementadores de la tabla que lo admitan agregar valor, especialmente para las tablas de contenido.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="c6cfa-115">Los implementadores de tabla que no admiten pueden devolver el valor MAPI_E_TOO_COMPLEX de una llamada **Restrict** o el valor MAPI_E_NOT_FOUND desde una llamada de **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="c6cfa-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="c6cfa-116">Los clientes deben tener en cuenta que, incluso si el proveedor admite restricciones en columnas no está en el conjunto actual de columna, va a obtener un mejor rendimiento general mediante la especificación de las columnas que se va a utilizar en sus restricciones con [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="c6cfa-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6cfa-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6cfa-117">See also</span></span>



[<span data-ttu-id="c6cfa-118">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6cfa-118">MAPI Tables</span></span>](mapi-tables.md)

