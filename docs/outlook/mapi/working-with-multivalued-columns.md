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
ms.openlocfilehash: 78f6083cf17bb21152df1a7ea09825f3be7f0e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572945"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="48622-103">Trabajar con columnas multivalor</span><span class="sxs-lookup"><span data-stu-id="48622-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="48622-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48622-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48622-105">Una columna multivalor contiene los datos de una propiedad multivalor, que es una propiedad que tiene una matriz de valores del tipo base en lugar de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="48622-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="48622-106">Debido a que ninguna de las tablas incluyen propiedades multivalor en sus conjuntos de columnas predeterminados, se incluyen propiedades multivalor en una tabla sólo si lo solicita el usuario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="48622-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="48622-107">Columnas con varios valores se pueden mostrar en las tablas:</span><span class="sxs-lookup"><span data-stu-id="48622-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="48622-108">En una sola fila, con todos los valores de propiedad que aparecen en la instancia de una sola columna.</span><span class="sxs-lookup"><span data-stu-id="48622-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="48622-109">Esto es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="48622-109">This is the default.</span></span>
    
    - <span data-ttu-id="48622-110">O bien -</span><span class="sxs-lookup"><span data-stu-id="48622-110">Or -</span></span>
    
- <span data-ttu-id="48622-111">En una serie de filas, con una fila para cada uno de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="48622-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="48622-112">Cada valor único aparece en la columna en su propia fila con allí es como número de filas como allí es valores de la propiedad multivalor.</span><span class="sxs-lookup"><span data-stu-id="48622-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="48622-113">Cada fila tiene un valor único para la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), pero los mismos valores para las demás columnas.</span><span class="sxs-lookup"><span data-stu-id="48622-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="48622-114">Si una fila contiene más de una columna con varios valores, por ejemplo, dos columnas con _M_ y _N_ valores respectivamente, a continuación, _M\*N_ instancias de la fila que aparecen en la tabla.</span><span class="sxs-lookup"><span data-stu-id="48622-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="48622-115">Un usuario de la tabla solicita el tipo que no sean predeterminadas de presentación llamando al método [IMAPITable::SetColumns](imapitable-setcolumns.md) con el indicador MVI_FLAG establecido en el tipo de propiedad de la columna multivalor.</span><span class="sxs-lookup"><span data-stu-id="48622-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="48622-116">El indicador MVI_FLAG es una constante definida como resultado de la combinación de los indicadores MV_FLAG y MV_INSTANCE con una operación **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="48622-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="48622-117">Además de su uso en **SetColumns**, MVI_FLAG también se pueden pasar a [SortTable](imapitable-sorttable.md) en el parámetro _lpSortCriteria_ e [IMAPITable:: Restrict](imapitable-restrict.md) en el miembro **ulPropTag** de la _lpRestriction_ parámetro.</span><span class="sxs-lookup"><span data-stu-id="48622-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="48622-118">Cuando se pasa el MVI_FLAG, **SortTable** realiza de forma similar a **SetColumns**, adición de una fila por cada valor en la columna multivalor y ordenar según los valores de las instancias de único.</span><span class="sxs-lookup"><span data-stu-id="48622-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="48622-119">Se agrega una fila para cada valor.</span><span class="sxs-lookup"><span data-stu-id="48622-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="48622-120">**Restrict**, sin embargo, no se expande la columna multivalor en filas calculadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="48622-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="48622-121">Una columna multivalor con el conjunto MVI_FLAG indica que el proveedor de servicios para usar esa columna en la restricción a la tabla.</span><span class="sxs-lookup"><span data-stu-id="48622-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="48622-122">Si hay un valor de propiedad en la restricción, debe ser una etiqueta de propiedad de valor único idéntica al que devolvería [IMAPITable:: QueryRows](imapitable-queryrows.md) para la columna.</span><span class="sxs-lookup"><span data-stu-id="48622-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="48622-123">Tabla sólo son necesarios para admitir el tipo de presentación predeterminado e implementadores pueden devolver el valor MAPI_E_TOO_COMPLEX cuando un llamador solicita la otra alternativa.</span><span class="sxs-lookup"><span data-stu-id="48622-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="48622-124">La capacidad para admitir ambos tipos de presentación es más importante para los proveedores de almacén de mensaje que se implementan las tablas de contenido de carpeta.</span><span class="sxs-lookup"><span data-stu-id="48622-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48622-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="48622-125">See also</span></span>



[<span data-ttu-id="48622-126">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="48622-126">MAPI Tables</span></span>](mapi-tables.md)

