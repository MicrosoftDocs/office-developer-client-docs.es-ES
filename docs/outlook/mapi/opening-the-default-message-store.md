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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348604"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="f618a-103">Abrir el almacén de mensajes predeterminado</span><span class="sxs-lookup"><span data-stu-id="f618a-103">Opening the default message store</span></span>

<span data-ttu-id="f618a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f618a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f618a-105">En cualquier sesión en particular, un almacén de mensajes actúa como almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f618a-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="f618a-106">Un almacén de mensajes predeterminado tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="f618a-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="f618a-107">La propiedad **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) se establece en true.</span><span class="sxs-lookup"><span data-stu-id="f618a-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="f618a-108">La marca STATUS_DEFAULT_STORE se establece en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f618a-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="f618a-109">MAPI crea automáticamente el subárbol IPM y las carpetas raíz para los resultados de la búsqueda, las vistas comunes y las vistas personales cuando se abre el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f618a-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="f618a-110">Para obtener más información acerca de estas carpetas, vea [IPM SUBTREE](ipm-subtree.md) y [MAPI Special folders](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="f618a-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="f618a-111">Para recuperar el identificador de entrada para el almacén de mensajes predeterminado, debe llamar a [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir la tabla de almacén de mensajes y aplicar una restricción adecuada en una llamada a [HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="f618a-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="f618a-112">**HrQueryAllRows** devolverá un conjunto de filas con la fila que representa el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f618a-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="f618a-113">La restricción que se pasa a **HrQueryAllRows** puede realizarse en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="f618a-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="f618a-114">Una restricción **and** que usa una estructura **SAndRestriction** para combinar:</span><span class="sxs-lookup"><span data-stu-id="f618a-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="f618a-115">Una restricción de EXISTS que usa una estructura **SExistRestriction** para comprobar la existencia de la propiedad **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="f618a-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="f618a-116">Una restricción de propiedad que usa una estructura [SPropertyRestriction](spropertyrestriction.md) para comprobar el valor true en la propiedad **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="f618a-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="f618a-117">Una restricción de máscara de subred que usa una estructura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como máscara en la propiedad **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="f618a-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f618a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f618a-118">See also</span></span>

- [<span data-ttu-id="f618a-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="f618a-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="f618a-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="f618a-120">SAndRestriction</span></span>](sandrestriction.md)

