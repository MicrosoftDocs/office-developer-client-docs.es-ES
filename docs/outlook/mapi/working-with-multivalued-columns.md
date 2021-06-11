---
title: Trabajar con columnas multivalor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420188"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="8ffb1-103">Trabajar con columnas multivalor</span><span class="sxs-lookup"><span data-stu-id="8ffb1-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="8ffb1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ffb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ffb1-105">Una columna multivalor contiene los datos de una propiedad multivalor, que es una propiedad que tiene una matriz de valores del tipo base en lugar de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="8ffb1-106">Dado que ninguna de las tablas incluye propiedades multivalor en sus conjuntos de columnas predeterminados, las propiedades multivalor solo se incluyen en una tabla si el usuario de la tabla lo solicita.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="8ffb1-107">Las columnas multivalor se pueden mostrar en tablas:</span><span class="sxs-lookup"><span data-stu-id="8ffb1-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="8ffb1-108">En una sola fila, con todos los valores de propiedad que aparecen en la instancia de una sola columna.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="8ffb1-109">Este valor es predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-109">This is the default.</span></span>
    
    - <span data-ttu-id="8ffb1-110">O -</span><span class="sxs-lookup"><span data-stu-id="8ffb1-110">Or -</span></span>
    
- <span data-ttu-id="8ffb1-111">En una serie de filas, con una fila para cada uno de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="8ffb1-112">Cada valor único aparece en la columna en su propia fila con tantas filas como valores en la propiedad multivalor.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="8ffb1-113">Cada fila tiene un valor único para la **propiedad PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), pero los mismos valores para las otras columnas.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="8ffb1-114">Si una fila contiene más de una columna con varios valores, por ejemplo, dos columnas con valores  _M_ y  _N_ respectivamente, las instancias  _M \* N_ de la fila aparecen en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="8ffb1-115">Un usuario de tabla solicita el tipo de presentación no predeterminado llamando al método [IMAPITable::SetColumns](imapitable-setcolumns.md) con la marca MVI_FLAG establecida en el tipo de propiedad de la columna multivalor.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="8ffb1-116">La MVI_FLAG marca es una constante definida como el resultado de combinar las marcas MV_FLAG y MV_INSTANCE con una operación **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="8ffb1-117">Además de usarse en **SetColumns**, MVI_FLAG también se puede pasar a [IMAPITable::SortTable](imapitable-sorttable.md) en el parámetro _lpSortCriteria_ y [IMAPITable::Restrict](imapitable-restrict.md) en el **miembro ulPropTag** del parámetro _lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="8ffb1-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="8ffb1-118">Cuando se pasa el MVI_FLAG, **SortTable** funciona de forma similar a **SetColumns**, agregando una fila por cada valor de la columna multivalor y ordenando en los valores únicos de las instancias.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="8ffb1-119">Se agrega una fila para cada valor.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="8ffb1-120">**Restrict,** sin embargo, no expande la columna multivalor en filas calculadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="8ffb1-121">Una columna multivalor con el conjunto MVI_FLAG indica al proveedor de servicios que use esa columna para restringir la tabla.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="8ffb1-122">Si hay un valor de propiedad en la restricción, debe ser una etiqueta de propiedad de valor único idéntica a la que [devolvería IMAPITable::QueryRows](imapitable-queryrows.md) para la columna.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="8ffb1-123">Los implementadores de tablas solo son necesarios para admitir el tipo de presentación predeterminado y pueden devolver el MAPI_E_TOO_COMPLEX cuando un autor de la llamada solicita la otra alternativa.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="8ffb1-124">La capacidad de admitir ambos tipos de presentación es lo más importante para los proveedores de almacén de mensajes que implementan tablas de contenido de carpetas.</span><span class="sxs-lookup"><span data-stu-id="8ffb1-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ffb1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ffb1-125">See also</span></span>



[<span data-ttu-id="8ffb1-126">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="8ffb1-126">MAPI Tables</span></span>](mapi-tables.md)

