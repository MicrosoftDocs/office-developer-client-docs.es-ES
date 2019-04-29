---
title: Sugerencias para trabajar con tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439740"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="831c5-103">Sugerencias para trabajar con tablas</span><span class="sxs-lookup"><span data-stu-id="831c5-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="831c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="831c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="831c5-105">Trabajar con una tabla MAPI es un poco como trabajar con una tabla de base de datos relacional.</span><span class="sxs-lookup"><span data-stu-id="831c5-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="831c5-106">Un usuario puede limitar el número de filas y columnas de la vista y especificar su orden.</span><span class="sxs-lookup"><span data-stu-id="831c5-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="831c5-107">Las filas se pueden recuperar de una en una o en grupos.</span><span class="sxs-lookup"><span data-stu-id="831c5-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="831c5-108">Un cursor que realiza un seguimiento de la posición actual puede moverse a un lugar específico de la tabla.</span><span class="sxs-lookup"><span data-stu-id="831c5-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="831c5-109">Para trabajar con tablas, los clientes usan la interfaz de solo lectura, [IMAPITable: IUnknown](imapitableiunknown.md), mientras que los proveedores de servicios, dependiendo de si son propietarios de los datos en los que se basa la tabla, pueden usar el **IMAPITable** o [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="831c5-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="831c5-110">Las operaciones definidas en estas interfaces se pueden clasificar como operaciones que todos los usuarios de tablas realizan o pueden invocar y operaciones que no se usan tan generalizadas porque son más avanzadas.</span><span class="sxs-lookup"><span data-stu-id="831c5-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="831c5-111">Algunas de las operaciones avanzadas son más complejas de implementar; otras no son más complejas, pero son de interés para una pequeña minoría de componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="831c5-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="831c5-112">Las operaciones más comunes son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="831c5-112">The more common operations are:</span></span>
  
- <span data-ttu-id="831c5-113">Operaciones de columna, que afectan a columnas únicas.</span><span class="sxs-lookup"><span data-stu-id="831c5-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="831c5-114">Incluyen la especificación de las propiedades que se van a incluir en el conjunto de columnas y el orden en que deben incluirse.</span><span class="sxs-lookup"><span data-stu-id="831c5-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="831c5-115">Operaciones de fila que afectan a filas individuales.</span><span class="sxs-lookup"><span data-stu-id="831c5-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="831c5-116">Entre ellas se incluyen la recuperación de datos y las operaciones de mantenimiento: agregar, eliminar y modificar una fila o filas individuales.</span><span class="sxs-lookup"><span data-stu-id="831c5-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="831c5-117">Operaciones globales, que afectan a toda la tabla.</span><span class="sxs-lookup"><span data-stu-id="831c5-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="831c5-118">Entre estos se incluyen la notificación de eventos, la búsqueda y la ordenación.</span><span class="sxs-lookup"><span data-stu-id="831c5-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="831c5-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="831c5-119">See also</span></span>



[<span data-ttu-id="831c5-120">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="831c5-120">MAPI Tables</span></span>](mapi-tables.md)

