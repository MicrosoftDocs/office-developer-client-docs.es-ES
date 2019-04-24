---
title: Representar datos adJuntos en texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280363"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="cf4de-103">Representar datos adJuntos en texto RTF</span><span class="sxs-lookup"><span data-stu-id="cf4de-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="cf4de-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf4de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf4de-105">Los clientes compatibles con el formato de texto enriquecido (RTF) pueden recuperar información de posición de representación a partir del texto del mensaje RTF buscando la siguiente secuencia de escape en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje:</span><span class="sxs-lookup"><span data-stu-id="cf4de-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="cf4de-106">**Para buscar información de representación en texto con formato**</span><span class="sxs-lookup"><span data-stu-id="cf4de-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="cf4de-107">Llame a **IMessage:: GetAttachmentTable** para obtener acceso a la tabla de datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf4de-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="cf4de-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="cf4de-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="cf4de-109">Cree una restricción de propiedad que limite la tabla a las filas que tienen **PR_RENDERING_POSITION** no igual a-1.</span><span class="sxs-lookup"><span data-stu-id="cf4de-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="cf4de-110">Para obtener más información, vea **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cf4de-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="cf4de-111">Llame al **IMAPITable:: Restrict** para exigir la restricción.</span><span class="sxs-lookup"><span data-stu-id="cf4de-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="cf4de-112">Para obtener más información, vea el [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="cf4de-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="cf4de-113">Llame al **IMAPITable:: SortTable** para ordenar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cf4de-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="cf4de-114">Para obtener más información, consulte [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="cf4de-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="cf4de-115">Llame al método **IMAPITable:: QueryRows** para recuperar las filas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="cf4de-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="cf4de-116">Para obtener más información, consulte [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="cf4de-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="cf4de-117">Llame al método **IMAPIProp:: OpenProperty** del mensaje para recuperar **PR_RTF_COMPRESSED** con la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cf4de-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="cf4de-118">Para obtener más información, vea [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="cf4de-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="cf4de-119">Examine la secuencia buscando el marcador de posición de representación, `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="cf4de-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="cf4de-120">El carácter que sigue a este marcador de posición es el espacio para los siguientes datos adjuntos de la tabla ordenada.</span><span class="sxs-lookup"><span data-stu-id="cf4de-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

