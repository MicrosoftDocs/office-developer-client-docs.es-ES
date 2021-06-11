---
title: Acerca de las restricciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433111"
---
# <a name="about-restrictions"></a><span data-ttu-id="05e88-103">Acerca de las restricciones</span><span class="sxs-lookup"><span data-stu-id="05e88-103">About Restrictions</span></span>

  
  
<span data-ttu-id="05e88-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05e88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05e88-105">Una restricción es una forma de limitar el número de filas de una vista a solo aquellas filas con valores para columnas que coinciden con criterios específicos.</span><span class="sxs-lookup"><span data-stu-id="05e88-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="05e88-106">Hay muchas oportunidades diferentes para usar restricciones con tablas.</span><span class="sxs-lookup"><span data-stu-id="05e88-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="05e88-107">Las aplicaciones cliente pueden usar restricciones, por ejemplo, para filtrar una tabla de contenido para los mensajes enviados por una persona determinada, para buscar filas que no admiten una propiedad o han establecido una propiedad en un valor específico, o para buscar destinatarios duplicados dentro de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="05e88-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="05e88-108">Los [métodos IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::FindRow](imapitable-findrow.md) se usan para establecer restricciones en una tabla.</span><span class="sxs-lookup"><span data-stu-id="05e88-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="05e88-109">**Restrict** aplica la restricción a la tabla sin recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="05e88-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="05e88-110">Para recuperar solo las filas que cumplen la restricción, se requiere una llamada posterior a [IMAPITable::QueryRows](imapitable-queryrows.md) o a un método similar.</span><span class="sxs-lookup"><span data-stu-id="05e88-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="05e88-111">**FindRow** aplica la restricción y recupera la primera fila de la tabla que coincide con los criterios.</span><span class="sxs-lookup"><span data-stu-id="05e88-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="05e88-112">**FindRow** aplica una restricción temporal, que solo existe durante la llamada, mientras que **Restrict** aplica una restricción más permanente.</span><span class="sxs-lookup"><span data-stu-id="05e88-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="05e88-113">Algunos clientes pueden crear una restricción mediante columnas que no están en el conjunto de columnas actual.</span><span class="sxs-lookup"><span data-stu-id="05e88-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="05e88-114">Admitir esta restricción es opcional y los implementadores de tablas que sí lo admiten agregan valor, especialmente para las tablas de contenido.</span><span class="sxs-lookup"><span data-stu-id="05e88-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="05e88-115">Los implementadores de tablas que no lo admiten pueden devolver el MAPI_E_TOO_COMPLEX de una llamada **Restrict** o el MAPI_E_NOT_FOUND de una **llamada FindRow.**</span><span class="sxs-lookup"><span data-stu-id="05e88-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="05e88-116">Los clientes deben tener en cuenta que, incluso si el proveedor admite restricciones en columnas que no están en el conjunto de columnas actual, tendrán un mejor rendimiento general especificando las columnas que pretenden usar en sus restricciones con [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="05e88-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05e88-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="05e88-117">See also</span></span>



[<span data-ttu-id="05e88-118">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="05e88-118">MAPI Tables</span></span>](mapi-tables.md)

