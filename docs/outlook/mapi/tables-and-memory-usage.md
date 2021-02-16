---
title: Uso de memoria y tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436863"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="a0d4b-103">Uso de memoria y tablas</span><span class="sxs-lookup"><span data-stu-id="a0d4b-103">Tables and memory usage</span></span>

<span data-ttu-id="a0d4b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0d4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0d4b-105">Un problema importante relacionado con la recuperación de datos de una tabla es el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="a0d4b-106">La falta de memoria disponible puede provocar un error [en IMAPITable::QueryRows](imapitable-queryrows.md) y [HrQueryAllRows,](hrqueryallrows.md) lo que devuelve un número menor que el número de filas deseado.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="a0d4b-107">Decidir qué método o función usar para recuperar datos de tabla depende de si se puede esperar que la tabla se ajuste a la memoria y, si no es posible, si el error es aceptable.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="a0d4b-108">Dado que no siempre es fácil determinar la cantidad de datos que caben en la memoria a la vez, MAPI proporciona algunas directrices básicas para que siga una aplicación cliente o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="a0d4b-109">Recuerde que siempre hay excepciones, en función de la implementación de tabla concreta y de cómo se almacenan los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="a0d4b-110">Se pueden usar las siguientes instrucciones para evaluar el uso de memoria de tabla:</span><span class="sxs-lookup"><span data-stu-id="a0d4b-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="a0d4b-111">Clientes que pueden tolerar el uso de memoria de conjunto de trabajo ocasional en el intervalo de megabytes y pueden suponer que no tendrán problemas al leer una tabla completa en la memoria.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="a0d4b-112">Las restricciones afectan al uso de memoria de una tabla.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="a0d4b-113">Se puede esperar que una tabla con restricciones graves con un gran número de filas, como una tabla de contenido, se ajuste a la memoria, mientras que una tabla grande sin restricciones normalmente no puede.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="a0d4b-114">Varias de las tablas que pertenecen a MAPI, como las tablas de estado, perfil, servicio de mensajes, proveedor y almacén de mensajes, normalmente caben en la memoria.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="a0d4b-115">Por lo general, se trata de tablas pequeñas.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-115">These are generally small tables.</span></span> <span data-ttu-id="a0d4b-116">Sin embargo, hay excepciones.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-116">However, there are exceptions.</span></span> <span data-ttu-id="a0d4b-117">Por ejemplo, un proveedor de perfiles basado en servidor podría generar una tabla de perfiles más grande que no se pueda ajustar.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="a0d4b-118">Para recuperar todas las filas de una tabla que caben en la memoria sin problemas, llame a [HrQueryAllRows](hrqueryallrows.md), estableciendo el número máximo de filas en cero.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="a0d4b-119">Para recuperar todas las filas de una tabla que podrían o no caben en la memoria, lo que genera un error, llame a **HrQueryAllRows** especificando un número máximo de filas.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="a0d4b-120">El número máximo de filas debe establecerse en un número mayor que el número mínimo de filas que se necesitan.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="a0d4b-121">Si un cliente debe tener acceso al menos a 50 filas de una tabla de 300 filas, el número máximo de filas debe establecerse en al menos 51.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="a0d4b-122">Para recuperar todas las filas de una tabla que no se espera que quepa en la memoria, llame a [IMAPITable::QueryRows](imapitable-queryrows.md) en un bucle con un recuento de filas relativamente pequeño, como se muestra en el siguiente ejemplo de código:</span><span class="sxs-lookup"><span data-stu-id="a0d4b-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="a0d4b-123">Cuando este bucle se completa y se han procesado todas las filas de la tabla y  _cRows_ es cero, la posición del cursor normalmente estará en la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a0d4b-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0d4b-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a0d4b-124">See also</span></span>

- [<span data-ttu-id="a0d4b-125">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="a0d4b-125">MAPI Tables</span></span>](mapi-tables.md)

