---
title: Sincronizar texto y formato
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346602"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="aa158-103">Sincronizar texto y formato</span><span class="sxs-lookup"><span data-stu-id="aa158-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="aa158-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa158-105">El desafío principal de enviar mensajes con formato de texto enriquecido (RTF) es mantener el texto sincronizado con el formato.</span><span class="sxs-lookup"><span data-stu-id="aa158-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="aa158-106">Para asegurarse de que cuando los mensajes llegan a su destino son como sus originadores y que el texto y el formato están sincronizados, MAPI proporciona la función [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="aa158-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="aa158-107">Los clientes que reconocen RTF suelen llamar a **RTFSync** antes de mostrar los mensajes entrantes y de la cola de impresión MAPI cuando descarga mensajes a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="aa158-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="aa158-108">Los autores de las llamadas especifican el área de posible discrepancia pasando una o dos marcas a **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="aa158-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="aa158-109">RTF_SYNC_BODY_CHANGED para indicar una modificación en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="aa158-110">RTF_SYNC_RTF_CHANGED para indicar una modificación en el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="aa158-111">El proceso de sincronización que se produce en **RTFSync** es una sofisticada comprobación de redundancia cíclica (CRC) del texto del mensaje que ignora algunos caracteres y convierte a otros.</span><span class="sxs-lookup"><span data-stu-id="aa158-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="aa158-112">Se omiten los caracteres que más probabilidades han agregado los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="aa158-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="aa158-113">MAPI define varias propiedades para trabajar con RTF como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa158-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="aa158-114">**Propiedad RTF**</span><span class="sxs-lookup"><span data-stu-id="aa158-114">**RTF property**</span></span>|<span data-ttu-id="aa158-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa158-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa158-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa158-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa158-117">Indica el principio del texto real del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="aa158-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa158-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa158-119">Contiene el resultado de la comprobación de redundancia cíclica del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="aa158-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa158-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa158-121">Contiene el número de caracteres en **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="aa158-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="aa158-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa158-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa158-123">Se establece en TRUE cuando se han sincronizado el texto y el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="aa158-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa158-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa158-125">Contiene el número de caracteres nonwhitespace que preceden al texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="aa158-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa158-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa158-127">Contiene el número de caracteres nonwhitespace que finalizan el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa158-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

