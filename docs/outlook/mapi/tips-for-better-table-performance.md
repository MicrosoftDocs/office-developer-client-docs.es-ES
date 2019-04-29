---
title: Sugerencias para mejorar el rendimiento de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412516"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="64ac0-103">Sugerencias para mejorar el rendimiento de tabla</span><span class="sxs-lookup"><span data-stu-id="64ac0-103">Tips for better table performance</span></span>
  
<span data-ttu-id="64ac0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64ac0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64ac0-105">Debido a que muchas de las operaciones de tabla pueden llevar mucho tiempo y no hay forma de indicar el progreso, es útil usar las siguientes técnicas para mejorar el rendimiento:</span><span class="sxs-lookup"><span data-stu-id="64ac0-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="64ac0-106">**Realizar el método [IMAPITable:](imapitableiunknown.md) las llamadas a IUnknown en el orden correcto**</span><span class="sxs-lookup"><span data-stu-id="64ac0-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="64ac0-107">Los clientes y los proveedores de servicios pueden trabajar con tablas de varias formas.</span><span class="sxs-lookup"><span data-stu-id="64ac0-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="64ac0-108">Pueden abrir la tabla y recuperar los datos de todas las filas con el conjunto de columnas y el criterio de ordenación predeterminados.</span><span class="sxs-lookup"><span data-stu-id="64ac0-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="64ac0-109">Como alternativa, pueden modificar esta vista predeterminada de la tabla cambiando el conjunto de columnas, cambiando el criterio de ordenación o estableciendo una restricción para restringir el ámbito de la tabla.</span><span class="sxs-lookup"><span data-stu-id="64ac0-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="64ac0-110">Las tablas que los usuarios intentan realizar una o varias de estas operaciones antes de recuperar los datos deben realizarse en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="64ac0-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="64ac0-111">Defina un conjunto de columnas con [IMAPITable:: SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="64ac0-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="64ac0-112">Establezca una restricción con el [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="64ac0-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="64ac0-113">Definir un criterio de ordenación con [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="64ac0-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="64ac0-114">La realización de estas tareas en este orden limita el número de filas y columnas que se van a ordenar, lo que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="64ac0-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="64ac0-115">**ReTrasar una operación mediante la marca TBL_BATCH, si es posible**</span><span class="sxs-lookup"><span data-stu-id="64ac0-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="64ac0-116">Si se establece\_la marca de lote de tbl en un método, el implementador de tablas puede recopilar varias llamadas antes de actuar en una de ellas.</span><span class="sxs-lookup"><span data-stu-id="64ac0-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="64ac0-117">En lugar de realizar potencialmente muchas llamadas a un servidor remoto; un implementador de tablas puede realizar uno, realizando todas las operaciones al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="64ac0-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="64ac0-118">Los resultados de las operaciones no se evalúan hasta que se necesitan.</span><span class="sxs-lookup"><span data-stu-id="64ac0-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="64ac0-119">Por ejemplo, cuando un cliente llama a [IMAPITable:: Restrict](imapitable-restrict.md) para especificar una restricción con el\_indicador de lote de tbl, la restricción no tiene que entrar en vigor hasta que el cliente llame a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="64ac0-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="64ac0-120">Esto permite que el implementador de tablas Combine el trabajo de dos llamadas en una.</span><span class="sxs-lookup"><span data-stu-id="64ac0-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="64ac0-121">Los usuarios de la tabla que se beneficien de la marca de lote de TBL\_deben tener en cuenta que el control de errores en estas condiciones puede ser más complejo.</span><span class="sxs-lookup"><span data-stu-id="64ac0-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="64ac0-122">Como controlar los errores de una operación retrasada es similar a controlar los errores cuando se\_establece la marca MAPI DEFERRED_ERRORS, vea difiriendo [MAPI Errors](deferring-mapi-errors.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="64ac0-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="64ac0-123">**Mantener una caché de las propiedades más usadas**</span><span class="sxs-lookup"><span data-stu-id="64ac0-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="64ac0-124">Los proveedores de servicios que implementan tablas pueden reducir el tiempo que se tarda en crear una vista mediante el almacenamiento en caché de las propiedades de objeto usadas con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="64ac0-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="64ac0-125">Al mantener una copia de estas propiedades en la memoria, se evita tener que recuperarlas del objeto cada vez que se debe volver a crear la vista.</span><span class="sxs-lookup"><span data-stu-id="64ac0-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64ac0-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="64ac0-126">See also</span></span>

- [<span data-ttu-id="64ac0-127">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="64ac0-127">MAPI Tables</span></span>](mapi-tables.md)

