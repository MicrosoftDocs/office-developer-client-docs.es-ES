---
title: Las tablas y el uso de memoria
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820849"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="1ffc9-103">Las tablas y el uso de memoria</span><span class="sxs-lookup"><span data-stu-id="1ffc9-103">Tables and memory usage</span></span>

<span data-ttu-id="1ffc9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ffc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ffc9-105">Un problema importante conectado con la recuperación de datos de una tabla es el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="1ffc9-106">Falta de memoria disponible puede provocar [IMAPITable:: QueryRows](imapitable-queryrows.md) y [HrQueryAllRows](hrqueryallrows.md) se lleve a cabo, devolución de menor que el número de filas que desee.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="1ffc9-107">Decidir qué método o función que se usará para recuperar los datos de la tabla depende de si la tabla puede esperarse que caben en la memoria y, si no se puede, si el error es aceptable.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="1ffc9-108">Dado que no siempre es fácil determinar la cantidad de datos que quepan en la memoria a la vez, MAPI proporciona algunas directrices básicas para una aplicación cliente o el proveedor de servicios que se deben seguir.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="1ffc9-109">Recuerde que siempre hay excepciones, en función de la implementación de una tabla determinada y cómo se almacenan los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="1ffc9-110">Las siguientes instrucciones se pueden usar para evaluar el uso de memoria de tabla:</span><span class="sxs-lookup"><span data-stu-id="1ffc9-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="1ffc9-111">Los clientes que pueden tolerar la ocasionales el uso de memoria conjunto de trabajo en el intervalo de megabyte y pueden asumir no tendrán ningún problema leer toda la tabla en la memoria.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="1ffc9-112">Restricciones tienen un efecto sobre el uso de una tabla de memoria.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="1ffc9-113">Una tabla rigurosamente restringida con un amplio número de filas, como una tabla de contenido, puede esperarse que caben en la memoria, mientras que normalmente no una tabla de gran tamaño sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="1ffc9-114">Varias de las tablas que pertenecen a MAPI, como el estado, perfiles, servicio de mensajes, proveedor y tablas de almacén de mensajes, normalmente quepan en la memoria.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="1ffc9-115">Estos son tablas pequeñas en general.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-115">These are generally small tables.</span></span> <span data-ttu-id="1ffc9-116">Sin embargo, hay excepciones.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-116">However, there are exceptions.</span></span> <span data-ttu-id="1ffc9-117">Por ejemplo, un proveedor de perfil basado en servidor podría generar una tabla de perfil de mayor tamaño que no pueda ajustar.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="1ffc9-118">Para recuperar todas las filas de una tabla que quepan en la memoria sin problemas, llame a [HrQueryAllRows](hrqueryallrows.md), si se establece el número máximo de filas en cero.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="1ffc9-119">Para recuperar todas las filas de una tabla que podría o no es posible que caben en la memoria, genere un error, llame a **HrQueryAllRows** especificando un número máximo de filas.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="1ffc9-120">El número máximo de filas debe establecerse en un número mayor que el número mínimo de filas que se necesitan.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="1ffc9-121">Si un cliente debe tener acceso al menos 50 filas de una tabla de 300 filas, el número máximo de filas debe establecerse en al menos 51.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="1ffc9-122">Para recuperar todas las filas de una tabla que no se espera que caben en la memoria, llamada [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle con un recuento de filas relativamente pequeño, como se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="1ffc9-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

<span data-ttu-id="1ffc9-123">Cuando se complete este bucle y se hayan procesado todas las filas de la tabla y _cRows_ es cero, normalmente será la posición del cursor en la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ffc9-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="1ffc9-124">See also</span></span>

- [<span data-ttu-id="1ffc9-125">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ffc9-125">MAPI Tables</span></span>](mapi-tables.md)

