---
title: Recuperar datos de filas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328661"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="b6046-103">Recuperar datos de filas de tabla</span><span class="sxs-lookup"><span data-stu-id="b6046-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="b6046-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6046-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6046-105">La recuperación de filas de una tabla implica:</span><span class="sxs-lookup"><span data-stu-id="b6046-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="b6046-106">Obtener los valores de propiedad de todas las columnas.</span><span class="sxs-lookup"><span data-stu-id="b6046-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="b6046-107">Modificación de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="b6046-107">Modifying the current position.</span></span>
    
<span data-ttu-id="b6046-108">Una de las columnas necesarias en la mayoría de las tablas es un identificador de \*\*\*\* entrada (la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)) que se puede usar para abrir el objeto que representa la fila.</span><span class="sxs-lookup"><span data-stu-id="b6046-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="b6046-109">Este identificador de entrada suele ser un identificador de entrada a corto plazo, uno que no persiste más allá de la duración de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b6046-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="b6046-110">Sin embargo, puede ser un identificador a largo plazo si el proveedor de servicios que implementa la tabla solo admite un tipo de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6046-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="b6046-111">Los clientes y los proveedores de servicios pueden realizar una de las siguientes llamadas para recuperar las filas:</span><span class="sxs-lookup"><span data-stu-id="b6046-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="b6046-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b6046-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="b6046-113">Recupera un número especificado de filas que comienzan con la fila actual en una dirección hacia delante o hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b6046-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="b6046-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b6046-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="b6046-115">Recupera todas las filas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="b6046-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="b6046-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="b6046-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="b6046-117">Recupera una fila de una tabla de acuerdo con el valor de su columna de índice.</span><span class="sxs-lookup"><span data-stu-id="b6046-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="b6046-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) suele ser la columna de índice de una tabla.</span><span class="sxs-lookup"><span data-stu-id="b6046-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="b6046-119">Cuando se incluye una propiedad opcional como una de las columnas de una tabla, es posible que algunas de las filas tengan valores válidos para la columna, mientras que otras no.</span><span class="sxs-lookup"><span data-stu-id="b6046-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="b6046-120">Si existe un valor válido para una columna depende de si el objeto que proporciona la información de la fila establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b6046-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="b6046-121">En función de la implementación del objeto, una propiedad que no existe puede representarse en la tabla como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) o un valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="b6046-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="b6046-122">Los usuarios de tablas deben tener cuidado para diferenciar entre propiedades que no existen y que tienen valores y propiedades sin significado que existen y tienen valores válidos.</span><span class="sxs-lookup"><span data-stu-id="b6046-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6046-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6046-123">See also</span></span>



[<span data-ttu-id="b6046-124">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="b6046-124">MAPI Tables</span></span>](mapi-tables.md)

