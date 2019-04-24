---
title: Mostrar una tabla de contenido de la carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339938"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="6bd7d-103">Mostrar una tabla de contenido de la carpeta</span><span class="sxs-lookup"><span data-stu-id="6bd7d-103">Displaying a folder contents table</span></span>

<span data-ttu-id="6bd7d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bd7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bd7d-105">La tabla de contenido de una carpeta contiene información de resumen sobre todos sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="6bd7d-106">La información de resumen sobre los nuevos mensajes entrantes aparece en la tabla de contenido de la carpeta de recepción para la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="6bd7d-107">Para que esta información esté disponible para los usuarios, recupere la tabla y muestre las columnas y las filas según corresponda.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="6bd7d-108">**Para mostrar una tabla de contenido de la carpeta**</span><span class="sxs-lookup"><span data-stu-id="6bd7d-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="6bd7d-109">Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md)y pase el identificador de entrada de la carpeta que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="6bd7d-110">Llame al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para abrir su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="6bd7d-111">Limite la vista de la tabla de contenido si lo desea, llamando al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la tabla para especificar determinadas columnas.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="6bd7d-112">Limite la vista de la tabla de contenido si lo desea, llamando al método [IMAPITable:: Restrict](imapitable-restrict.md) para filtrar determinadas filas.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="6bd7d-113">Si, por ejemplo, desea mostrar solo los mensajes con una clase de mensaje específica que todavía se ha leído:</span><span class="sxs-lookup"><span data-stu-id="6bd7d-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="6bd7d-114">Cree una restricción de propiedad en una estructura [SPropertyRestriction](spropertyrestriction.md) que coincida con la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) con la clase de mensaje deseada.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="6bd7d-115">Cree una restricción de máscara de subred en una estructura [SBitMaskRestriction](sbitmaskrestriction.md) que use **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como etiqueta de propiedad y el valor MSGFLAG_UNREAD como máscara.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="6bd7d-116">Cree una restricción en una estructura [SAndRestriction](sandrestriction.md) que combine las restricciones de propiedad y máscara de la máscara.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="6bd7d-117">Ordene la tabla de contenido si lo desea mediante una llamada al método [IMAPITable:: SortTable](imapitable-sorttable.md) de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="6bd7d-118">Llame al [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla de contenido para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

