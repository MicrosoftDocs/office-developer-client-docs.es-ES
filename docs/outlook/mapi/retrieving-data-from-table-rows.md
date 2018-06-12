---
title: Recuperación de datos de las filas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820525"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="f11ef-103">Recuperación de datos de las filas de tabla</span><span class="sxs-lookup"><span data-stu-id="f11ef-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="f11ef-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f11ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f11ef-105">Recuperación de filas de una tabla implica:</span><span class="sxs-lookup"><span data-stu-id="f11ef-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="f11ef-106">Obtención de los valores de propiedad para todas las columnas.</span><span class="sxs-lookup"><span data-stu-id="f11ef-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="f11ef-107">Modificación de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="f11ef-107">Modifying the current position.</span></span>
    
<span data-ttu-id="f11ef-108">Una de las columnas necesarias en la mayoría de las tablas es un identificador de entrada: la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), que se pueden utilizar para abrir el objeto que representa la fila.</span><span class="sxs-lookup"><span data-stu-id="f11ef-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="f11ef-109">Normalmente, este identificador de entrada es un identificador de entrada a corto plazo, uno que no se conserva más allá de la duración de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f11ef-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="f11ef-110">Sin embargo, puede ser un identificador a largo plazo si el proveedor de implementación de la tabla sólo admite un tipo de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="f11ef-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="f11ef-111">Los clientes y proveedores de servicios pueden realizar una de las llamadas para recuperar las filas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f11ef-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="f11ef-112">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="f11ef-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="f11ef-113">Recupera un número especificado de filas a partir de la fila actual en una dirección hacia delante o hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="f11ef-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="f11ef-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="f11ef-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="f11ef-115">Recupera todas las filas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="f11ef-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="f11ef-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="f11ef-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="f11ef-117">Recupera una fila en una tabla de acuerdo con el valor de su columna de índice.</span><span class="sxs-lookup"><span data-stu-id="f11ef-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="f11ef-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) generalmente es la columna de índice para una tabla.</span><span class="sxs-lookup"><span data-stu-id="f11ef-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="f11ef-119">Cuando una propiedad opcional se incluye como una de las columnas de una tabla, mientras que otros usuarios podrían no algunas de las filas deberían los valores válidos para la columna.</span><span class="sxs-lookup"><span data-stu-id="f11ef-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="f11ef-120">Si existe un valor válido para una columna depende de si la propiedad establece el objeto que proporciona la información de la fila.</span><span class="sxs-lookup"><span data-stu-id="f11ef-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="f11ef-121">Dependiendo de la implementación del objeto, se puede representar una propiedad que no existe en la tabla como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) o un valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f11ef-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="f11ef-122">Los usuarios de las tablas deben tener cuidados diferenciar entre las propiedades que existen y tienen valores sin sentido y las propiedades que existen y tienen valores válidos.</span><span class="sxs-lookup"><span data-stu-id="f11ef-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f11ef-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="f11ef-123">See also</span></span>



[<span data-ttu-id="f11ef-124">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="f11ef-124">MAPI Tables</span></span>](mapi-tables.md)

