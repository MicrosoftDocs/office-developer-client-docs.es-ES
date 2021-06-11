---
title: Abrir el almacén de mensajes predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436030"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="78101-103">Abrir el almacén de mensajes predeterminado</span><span class="sxs-lookup"><span data-stu-id="78101-103">Opening the default message store</span></span>

<span data-ttu-id="78101-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78101-105">En cualquier sesión en particular, un almacén de mensajes actúa como almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="78101-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="78101-106">Un almacén de mensajes predeterminado tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="78101-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="78101-107">La **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) se establece en TRUE.</span><span class="sxs-lookup"><span data-stu-id="78101-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="78101-108">La STATUS_DEFAULT_STORE se establece en la **propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="78101-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="78101-109">MAPI crea automáticamente el subárbol IPM y las carpetas raíz para resultados de búsqueda, vistas comunes y vistas personales cuando se abre el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="78101-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="78101-110">Para obtener más información acerca de estas carpetas, vea [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="78101-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="78101-111">Para recuperar el identificador de entrada del almacén de mensajes predeterminado, debe llamar a [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir la tabla del almacén de mensajes y aplicar una restricción adecuada en una llamada a [HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="78101-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="78101-112">**HrQueryAllRows** devolverá un conjunto de filas con la fila que representa el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="78101-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="78101-113">La restricción que se pasa a **HrQueryAllRows** puede tener uno de los siguientes formularios:</span><span class="sxs-lookup"><span data-stu-id="78101-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="78101-114">Una **restricción AND** que usa una estructura **SAndRestriction** para combinar:</span><span class="sxs-lookup"><span data-stu-id="78101-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="78101-115">Existe una restricción que usa una **estructura SExistRestriction** para probar la existencia de la **PR_DEFAULT_STORE** propiedad.</span><span class="sxs-lookup"><span data-stu-id="78101-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="78101-116">Una restricción de propiedad que usa una [estructura SPropertyRestriction](spropertyrestriction.md) para buscar el valor TRUE en la **PR_DEFAULT_STORE** propiedad.</span><span class="sxs-lookup"><span data-stu-id="78101-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="78101-117">Una restricción de máscara de bits que usa una estructura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como máscara en la **PR_RESOURCE_FLAGS** propiedad.</span><span class="sxs-lookup"><span data-stu-id="78101-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="78101-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="78101-118">See also</span></span>

- [<span data-ttu-id="78101-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="78101-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="78101-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="78101-120">SAndRestriction</span></span>](sandrestriction.md)

