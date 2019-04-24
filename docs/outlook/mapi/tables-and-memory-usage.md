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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320408"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="3ec19-103">Uso de memoria y tablas</span><span class="sxs-lookup"><span data-stu-id="3ec19-103">Tables and memory usage</span></span>

<span data-ttu-id="3ec19-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec19-105">Un problema importante conectado a la recuperación de datos de una tabla es el uso de la memoria.</span><span class="sxs-lookup"><span data-stu-id="3ec19-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="3ec19-106">La falta de memoria disponible puede provocar un error de [IMAPITable:: QueryRows](imapitable-queryrows.md) y [HrQueryAllRows](hrqueryallrows.md) , lo que devuelve un número inferior al número de filas deseado.</span><span class="sxs-lookup"><span data-stu-id="3ec19-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="3ec19-107">La decisión del método o la función que se va a usar para recuperar los datos de la tabla depende de si se puede esperar que la tabla quepa en la memoria y, si no es posible, si el error es aceptable.</span><span class="sxs-lookup"><span data-stu-id="3ec19-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="3ec19-108">Como no siempre es fácil determinar la cantidad de datos que se ajustarán a la memoria al mismo tiempo, MAPI proporciona instrucciones básicas para que el proveedor de servicios o aplicaciones cliente sigan.</span><span class="sxs-lookup"><span data-stu-id="3ec19-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="3ec19-109">Recuerde que siempre hay excepciones, basadas en la implementación de la tabla concreta y en la forma en que se almacenan los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="3ec19-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="3ec19-110">Las siguientes instrucciones pueden usarse para evaluar el uso de memoria de la tabla:</span><span class="sxs-lookup"><span data-stu-id="3ec19-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="3ec19-111">Clientes que pueden tolerar el uso de memoria del espacio de trabajo ocasional en el intervalo de megabytes y suponer que no tendrán problemas para leer una tabla completa en la memoria.</span><span class="sxs-lookup"><span data-stu-id="3ec19-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="3ec19-112">Las restricciones afectan al uso de memoria de una tabla.</span><span class="sxs-lookup"><span data-stu-id="3ec19-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="3ec19-113">Una tabla rigurosamente restringida con un amplio número de filas, como una tabla de contenido, puede esperarse que quepa en la memoria, mientras que una tabla grande sin restricciones no suele.</span><span class="sxs-lookup"><span data-stu-id="3ec19-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="3ec19-114">Normalmente, varias de las tablas que son propiedad de MAPI, como el estado, el perfil, el servicio de mensajes, el proveedor y las tablas de almacén de mensajes, se ajustan a la memoria.</span><span class="sxs-lookup"><span data-stu-id="3ec19-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="3ec19-115">Por lo general, son tablas pequeñas.</span><span class="sxs-lookup"><span data-stu-id="3ec19-115">These are generally small tables.</span></span> <span data-ttu-id="3ec19-116">Sin embargo, hay excepciones.</span><span class="sxs-lookup"><span data-stu-id="3ec19-116">However, there are exceptions.</span></span> <span data-ttu-id="3ec19-117">Por ejemplo, un proveedor de perfiles basado en servidor puede generar una tabla de perfiles más grande que no se podrá ajustar.</span><span class="sxs-lookup"><span data-stu-id="3ec19-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="3ec19-118">Para recuperar todas las filas de una tabla que se ajusten a la memoria sin problemas, llame a [HrQueryAllRows](hrqueryallrows.md), estableciendo el número máximo de filas en cero.</span><span class="sxs-lookup"><span data-stu-id="3ec19-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="3ec19-119">Para recuperar todas las filas de una tabla que puedan caber o no en la memoria, se genera un error y se llama a **HrQueryAllRows** especificando un número máximo de filas.</span><span class="sxs-lookup"><span data-stu-id="3ec19-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="3ec19-120">El número máximo de filas debe establecerse en un número mayor que el número mínimo de filas necesarias.</span><span class="sxs-lookup"><span data-stu-id="3ec19-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="3ec19-121">Si un cliente debe acceder a al menos 50 filas de una tabla de la fila 300, el número máximo de filas debe establecerse como mínimo en 51.</span><span class="sxs-lookup"><span data-stu-id="3ec19-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="3ec19-122">Para recuperar todas las filas de una tabla que no se espera que quepan en la memoria, llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle con un recuento de filas relativamente pequeño, como se ilustra en el siguiente ejemplo de código:</span><span class="sxs-lookup"><span data-stu-id="3ec19-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="3ec19-123">Cuando se complete este bucle y se hayan procesado todas las filas de la tabla, __ y Crows sea cero, la posición del cursor estará normalmente en la parte inferior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3ec19-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ec19-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ec19-124">See also</span></span>

- [<span data-ttu-id="3ec19-125">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="3ec19-125">MAPI Tables</span></span>](mapi-tables.md)

