---
title: Representación de datos adjuntos en texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439796"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="974ae-103">Representación de datos adjuntos en texto RTF</span><span class="sxs-lookup"><span data-stu-id="974ae-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="974ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="974ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="974ae-105">Los clientes con formato de texto enriquecido (RTF) pueden recuperar información de posición de representación del texto del mensaje RTF buscando la siguiente secuencia de escape en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje:</span><span class="sxs-lookup"><span data-stu-id="974ae-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="974ae-106">**Para localizar la información de representación en texto con formato**</span><span class="sxs-lookup"><span data-stu-id="974ae-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="974ae-107">Llame **a IMessage::GetAttachmentTable** para obtener acceso a la tabla de datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="974ae-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="974ae-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="974ae-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="974ae-109">Cree una restricción de propiedad que limite la tabla a las filas PR_RENDERING_POSITION **que** no son iguales a -1.</span><span class="sxs-lookup"><span data-stu-id="974ae-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="974ae-110">Para obtener más información, **vea PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="974ae-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="974ae-111">Llame **a IMAPITable::Restrict** para aplicar la restricción.</span><span class="sxs-lookup"><span data-stu-id="974ae-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="974ae-112">Para obtener más información, [vea IMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="974ae-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="974ae-113">Llame **a IMAPITable::SortTable** para ordenar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="974ae-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="974ae-114">Para obtener más información, [vea IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="974ae-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="974ae-115">Llame **a IMAPITable::QueryRows** para recuperar las filas apropiadas.</span><span class="sxs-lookup"><span data-stu-id="974ae-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="974ae-116">Para obtener más información, [vea IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="974ae-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="974ae-117">Llame al método **IMAPIProp::OpenProperty** del mensaje para recuperar **PR_RTF_COMPRESSED** con la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="974ae-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="974ae-118">Para obtener más información, [vea IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="974ae-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="974ae-119">Examinar la secuencia, buscando el marcador de posición de representación,  `\objattph` .</span><span class="sxs-lookup"><span data-stu-id="974ae-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="974ae-120">El carácter que sigue a este marcador de posición es el lugar para los siguientes datos adjuntos en la tabla ordenada.</span><span class="sxs-lookup"><span data-stu-id="974ae-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

