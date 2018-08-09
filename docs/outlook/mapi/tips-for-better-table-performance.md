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
ms.openlocfilehash: 2b14c4fe8cbbadb2ccdd6a2f7870a07d2f96a3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820861"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="a28d2-103">Sugerencias para mejorar el rendimiento de tabla</span><span class="sxs-lookup"><span data-stu-id="a28d2-103">Tips for better table performance</span></span>
  
<span data-ttu-id="a28d2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a28d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a28d2-105">Debido a que muchas de las operaciones de tabla pueden llevar mucho tiempo y no hay ninguna manera de indicar el progreso, es útil usar las siguientes técnicas para mejorar el rendimiento:</span><span class="sxs-lookup"><span data-stu-id="a28d2-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="a28d2-106">**Realizar [IMAPITable: IUnknown](imapitableiunknown.md) llama en el orden correcto**</span><span class="sxs-lookup"><span data-stu-id="a28d2-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="a28d2-107">Los clientes y proveedores de servicios pueden trabajar con tablas en una variedad de formas.</span><span class="sxs-lookup"><span data-stu-id="a28d2-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="a28d2-108">Puede abrir la tabla y recuperar los datos para todas las filas con el conjunto de columnas predeterminado y criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="a28d2-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="a28d2-109">Como alternativa, se puede modificar esta vista predeterminada de la tabla para cambiar el conjunto de columnas, cambiar el criterio de ordenación o establecer una restricción para limitar el ámbito de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a28d2-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="a28d2-110">Los usuarios de la tabla que se van a realizar una o varias de estas operaciones antes de recuperar los datos deben realizarlas en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="a28d2-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="a28d2-111">Definir una columna establecida con [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="a28d2-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="a28d2-112">Establecer una restricción con [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="a28d2-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="a28d2-113">Definir un criterio de ordenación con [SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="a28d2-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="a28d2-114">Llevar a cabo estas tareas en este orden, limita el número de filas y columnas que se va a ordenar, lo que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a28d2-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="a28d2-115">**Retraso de una operación utilizando la marca TBL_BATCH si es posible**</span><span class="sxs-lookup"><span data-stu-id="a28d2-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="a28d2-116">Establecer el TBL\_indicador de lote en un método permite al implementador tabla recopilar varias llamadas antes de actuar en uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="a28d2-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="a28d2-117">En lugar de realizar potencialmente muchas llamadas a un servidor remoto; un implementador de la tabla uno, puede hacer que realizan todas las operaciones a la vez.</span><span class="sxs-lookup"><span data-stu-id="a28d2-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="a28d2-118">Los resultados de las operaciones no se evalúan hasta que sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="a28d2-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="a28d2-119">Por ejemplo, cuando un cliente llama a [IMAPITable:: Restrict](imapitable-restrict.md) para especificar una restricción con el TBL\_por lotes indicador establecido, la restricción no es necesario que entran en efecto hasta que el cliente llama [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="a28d2-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="a28d2-120">Esto permite que el implementador de tabla combinar el trabajo de dos llamadas en uno.</span><span class="sxs-lookup"><span data-stu-id="a28d2-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="a28d2-121">La tabla de usuarios que permite aprovechar el TBL\_marca por lotes debe tener en cuenta que los errores en las siguientes condiciones pueden ser más complejo.</span><span class="sxs-lookup"><span data-stu-id="a28d2-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="a28d2-122">Debido a que controla los errores de una operación retrasada es similar a la gestión de los errores cuando el MAPI\_se establece la marca DEFERRED_ERRORS, consulte [Aplazamiento de errores de MAPI](deferring-mapi-errors.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a28d2-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="a28d2-123">**Mantener una memoria caché de propiedades usadas con más frecuencia**</span><span class="sxs-lookup"><span data-stu-id="a28d2-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="a28d2-124">Proveedores de servicios de implementación de las tablas pueden reducir el tiempo necesario para crear una vista mediante el almacenamiento en memoria caché copias de las propiedades del objeto usados con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="a28d2-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="a28d2-125">Es necesario recompilar conservar una copia de estas propiedades en ahorra memoria tener que recuperar desde el objeto cada vez que la vista.</span><span class="sxs-lookup"><span data-stu-id="a28d2-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a28d2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a28d2-126">See also</span></span>

- [<span data-ttu-id="a28d2-127">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="a28d2-127">MAPI Tables</span></span>](mapi-tables.md)

