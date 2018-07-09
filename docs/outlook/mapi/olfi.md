---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ff23472254df2bd9d2195c7cf2c4258b856ec430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818433"
---
# <a name="olfi"></a><span data-ttu-id="21d7c-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="21d7c-103">OLFI</span></span>

  
  
<span data-ttu-id="21d7c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21d7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21d7c-105">Cola de estructuras de identificador a largo plazo utilizado por el proveedor de almacén de carpetas personales (PST) para asignar un identificador de entrada para un nuevo mensaje o una carpeta en modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="21d7c-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="21d7c-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="21d7c-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="21d7c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="21d7c-107">Members</span></span>

 <span data-ttu-id="21d7c-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="21d7c-108">_ulVersion_</span></span>
  
- <span data-ttu-id="21d7c-109">Número de versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="21d7c-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="21d7c-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="21d7c-110">_muidReserved_</span></span>
  
- <span data-ttu-id="21d7c-111">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="21d7c-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="21d7c-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="21d7c-112">_ulReserved_</span></span>
  
- <span data-ttu-id="21d7c-113">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="21d7c-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="21d7c-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="21d7c-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="21d7c-115">El número de entradas que están disponibles para la asignación.</span><span class="sxs-lookup"><span data-stu-id="21d7c-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="21d7c-116">Estas entradas comparten el mismo identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="21d7c-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="21d7c-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="21d7c-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="21d7c-118">El número de entradas que están disponibles a continuación para la asignación.</span><span class="sxs-lookup"><span data-stu-id="21d7c-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="21d7c-119">Estas entradas comparten el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="21d7c-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="21d7c-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="21d7c-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="21d7c-121">A largo plazo ID estructura, **[LTID](ltid.md)**, que identifica la entrada actualmente disponible para la asignación.</span><span class="sxs-lookup"><span data-stu-id="21d7c-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="21d7c-122">La estructura de identificador a largo plazo contiene un GUID y un índice que identifica un objeto en el almacén.</span><span class="sxs-lookup"><span data-stu-id="21d7c-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="21d7c-123">Juntos, el GUID y el índice pueden forman un identificador único de entrada para un objeto.</span><span class="sxs-lookup"><span data-stu-id="21d7c-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="21d7c-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="21d7c-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="21d7c-125">Estructura de identificador que identifica la siguiente entrada disponible a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="21d7c-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21d7c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="21d7c-126">Remarks</span></span>

<span data-ttu-id="21d7c-127">Un identificador de entrada es un identificador de entrada MAPI de 4 bytes para una carpeta o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="21d7c-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="21d7c-128">Para obtener más información, vea la [propiedad ENTRYID](http://msdn.microsoft.com/es-es/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="21d7c-128">For more information, see [ENTRYID](http://msdn.microsoft.com/es-es/library/ms836424).</span></span>
  
<span data-ttu-id="21d7c-129">Cuando un proveedor de almacén de archivos PST, asigna un identificador de entrada a un nuevo objeto, primero necesita un GUID que identifica el servidor y un índice que identifica el objeto en el almacén.</span><span class="sxs-lookup"><span data-stu-id="21d7c-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="21d7c-130">Aunque el GUID no es único entre todos los identificadores de entrada, el GUID y el índice combinado proporcionan una única entrada.</span><span class="sxs-lookup"><span data-stu-id="21d7c-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="21d7c-131">Este par GUID y el índice se realiza un seguimiento por una estructura de identificador a largo plazo, **LTID**, que forma parte de la estructura **OLFI** .</span><span class="sxs-lookup"><span data-stu-id="21d7c-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="21d7c-132">El proveedor de almacén de archivos PST no físicamente tenga en **OLFI** una estructura **LTID** para cada pareja de índice del GUID.</span><span class="sxs-lookup"><span data-stu-id="21d7c-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="21d7c-133">Mantiene una estructura **LTID** , *ltidAlloc* , para el primer actualmente par GUID-índice disponible; un recuento, *dwAlloc* , el número de entradas disponibles que comparten este mismo GUID; y una segunda estructura **LTID** , *ltidNextAlloc* , para el siguiente par GUID-índice disponible que tiene un GUID diferente.</span><span class="sxs-lookup"><span data-stu-id="21d7c-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="21d7c-134">El archivo PST almacenar proveedor usa la estructura **OLFI** para realizar un seguimiento de los GUID y los índices que ha entregar. En un nivel virtual, el proveedor mantiene una reserva de un número de estructuras **LTID** que están listos para ser asignado.</span><span class="sxs-lookup"><span data-stu-id="21d7c-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="21d7c-135">*dwAlloc* mantiene un recuento de las estructuras **LTID** disponibles.</span><span class="sxs-lookup"><span data-stu-id="21d7c-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="21d7c-136">Las solicitudes de los identificadores de entrada se incluyen en bloques.</span><span class="sxs-lookup"><span data-stu-id="21d7c-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="21d7c-137">Cuando hay una solicitud de un bloque, el proveedor de almacén de archivos PST comprueba si hay suficiente reserva por parte comparando el tamaño solicitado con *dwAlloc* .</span><span class="sxs-lookup"><span data-stu-id="21d7c-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="21d7c-138">Si no hay suficiente reserva, devuelve el GUID y el índice en *ltidAlloc* para la asignación.</span><span class="sxs-lookup"><span data-stu-id="21d7c-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="21d7c-139">A continuación, se disminuye *dwAlloc* por el tamaño solicitado y se incrementa el índice en *ltidAlloc* en el tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="21d7c-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="21d7c-140">Esto prepara el proveedor de almacenamiento de PST asignar *ltidAlloc* en la siguiente solicitud para otro bloque de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="21d7c-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="21d7c-141">Tenga en cuenta que el GUID sigue siendo la misma para la solicitud siguiente.</span><span class="sxs-lookup"><span data-stu-id="21d7c-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="21d7c-142">Si el tamaño de una solicitud es mayor que *dwAlloc* , el proveedor de almacén de archivos PST intenta usar qué tiene a continuación en reserva, tal como se especifica por *dwNextAlloc* y *ltidNextAlloc* .</span><span class="sxs-lookup"><span data-stu-id="21d7c-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="21d7c-143">Copia *dwNextAlloc* y *ltidNextAlloc* en *dwAlloc* y *ltidAlloc* , respectivamente y *dwNextAlloc* y *ltidNextAlloc* se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="21d7c-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="21d7c-144">Un proveedor que se ajusta el proveedor de almacén de archivos PST debe comprobar periódicamente *ltidNextAlloc* para ver si es NULL.</span><span class="sxs-lookup"><span data-stu-id="21d7c-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="21d7c-145">Si es así, el proveedor debe rellenar con un nuevo GUID y restablecer *dwNextAlloc* de modo que se pueden asignar más identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="21d7c-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="21d7c-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="21d7c-146">See also</span></span>



[<span data-ttu-id="21d7c-147">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="21d7c-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="21d7c-148">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="21d7c-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="21d7c-149">LTID</span><span class="sxs-lookup"><span data-stu-id="21d7c-149">LTID</span></span>](ltid.md)

