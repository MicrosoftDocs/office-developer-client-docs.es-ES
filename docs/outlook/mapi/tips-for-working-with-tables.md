---
title: Sugerencias para trabajar con tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820853"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="101b9-103">Sugerencias para trabajar con tablas</span><span class="sxs-lookup"><span data-stu-id="101b9-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="101b9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="101b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="101b9-105">Trabajar con una MAPI tabla es un poco like trabajar con una tabla de base de datos relacional.</span><span class="sxs-lookup"><span data-stu-id="101b9-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="101b9-106">Un usuario puede limitar el número de filas y columnas en la vista y especificar su orden.</span><span class="sxs-lookup"><span data-stu-id="101b9-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="101b9-107">Filas pueden ser recuperado uno a la vez o en grupos.</span><span class="sxs-lookup"><span data-stu-id="101b9-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="101b9-108">Un cursor que realiza un seguimiento de la posición actual se puede mover a una ubicación específica en la tabla.</span><span class="sxs-lookup"><span data-stu-id="101b9-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="101b9-109">Para trabajar con tablas, los clientes usan la interfaz de sólo lectura, [IMAPITable: IUnknown](imapitableiunknown.md), mientras que los proveedores de servicios, dependiendo de si son propietarios de los datos que se basa en la tabla, pueden usar cualquier **IMAPITable** o [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="101b9-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="101b9-110">Las operaciones definidas en estas interfaces se pueden clasificar como operaciones que o pueden invocar todos los usuarios de las tablas y las operaciones que no se utilizan como ampliamente porque más avanzadas.</span><span class="sxs-lookup"><span data-stu-id="101b9-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="101b9-111">Algunas de las operaciones avanzadas son más complejas de implementar; otros usuarios no más complejas, pero son de interés para una minoría de componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="101b9-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="101b9-112">Las operaciones más comunes son:</span><span class="sxs-lookup"><span data-stu-id="101b9-112">The more common operations are:</span></span>
  
- <span data-ttu-id="101b9-113">Operaciones de columna, que afectan a columnas individuales.</span><span class="sxs-lookup"><span data-stu-id="101b9-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="101b9-114">Éstas incluyen la especificación de las propiedades que se deben incluir en el conjunto de columnas y el orden en el que se deben incluir.</span><span class="sxs-lookup"><span data-stu-id="101b9-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="101b9-115">Operaciones de fila, que afectan a filas individuales.</span><span class="sxs-lookup"><span data-stu-id="101b9-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="101b9-116">Entre estas incluyen la recuperación de datos y las operaciones de mantenimiento: adición, eliminación y modificación de una sola fila o las filas.</span><span class="sxs-lookup"><span data-stu-id="101b9-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="101b9-117">Operaciones globales que afectan a toda la tabla.</span><span class="sxs-lookup"><span data-stu-id="101b9-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="101b9-118">Éstas incluyen la notificación de eventos, búsqueda y la ordenación.</span><span class="sxs-lookup"><span data-stu-id="101b9-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="101b9-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="101b9-119">See also</span></span>



[<span data-ttu-id="101b9-120">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="101b9-120">MAPI Tables</span></span>](mapi-tables.md)

