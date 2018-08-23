---
title: Mostrar una tabla de contenido de carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51c88e8c062a409db305e893b82f43d8c8ac7094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580799"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="b2c1a-103">Mostrar una tabla de contenido de carpeta</span><span class="sxs-lookup"><span data-stu-id="b2c1a-103">Displaying a folder contents table</span></span>

<span data-ttu-id="b2c1a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2c1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2c1a-105">En la tabla de contenido de una carpeta contiene información de resumen sobre todos sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="b2c1a-106">Información de resumen acerca de los mensajes entrantes nuevo aparece en la tabla de contenido de la carpeta de recepción para la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="b2c1a-107">Para que esta información esté disponible para los usuarios, recuperar la tabla y mostrar las columnas y filas según corresponda.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="b2c1a-108">**Para mostrar una tabla de contenido de carpeta**</span><span class="sxs-lookup"><span data-stu-id="b2c1a-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="b2c1a-109">Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md), pasando el identificador de entrada de la carpeta que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="b2c1a-110">Llamar al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para abrir su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="b2c1a-111">Limitar la vista de la tabla de contenido si así lo desea mediante una llamada al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla para especificar columnas en particular.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="b2c1a-112">Limitar la vista de la tabla de contenido si así lo desea mediante una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) de la tabla para filtrar filas determinadas.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="b2c1a-113">Si, por ejemplo, que desea mostrar sólo los mensajes con una clase de mensaje específica que tienen aún se leerá:</span><span class="sxs-lookup"><span data-stu-id="b2c1a-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="b2c1a-114">Crear una restricción de propiedad en una estructura [SPropertyRestriction](spropertyrestriction.md) que coincida con la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) con la clase de mensaje que desee.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="b2c1a-115">Crear una restricción de máscara de bits en una estructura [SBitMaskRestriction](sbitmaskrestriction.md) que usa **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como la etiqueta de propiedad y el valor MSGFLAG_UNREAD como la máscara.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="b2c1a-116">Crear una restricción de una estructura de [SAndRestriction](sandrestriction.md) que se une a las restricciones de propiedad y la máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="b2c1a-117">Ordenar la tabla de contenido si así lo desea mediante una llamada al método de [SortTable](imapitable-sorttable.md) de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="b2c1a-118">Llamar a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla de contenido para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b2c1a-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

