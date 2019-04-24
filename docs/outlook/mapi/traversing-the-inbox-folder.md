---
title: Recorrer la carpeta Bandeja de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356584"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="168af-103">Recorrer la carpeta Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="168af-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="168af-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="168af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="168af-105">**Para recorrer todos los mensajes de la bandeja de entrada**</span><span class="sxs-lookup"><span data-stu-id="168af-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="168af-106">Llame a [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar el identificador de entrada de la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="168af-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="168af-107">Llame a **IMAPIFolder:: OpenEntry** para abrir la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="168af-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="168af-108">Llame al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la bandeja de entrada para recuperar la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="168af-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="168af-109">Llame al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la tabla de contenido para limitar la columna \*\*\*\* establecida como valor máximo ([PidTagEntryId](pidtagentryid-canonical-property.md)) y cualquier otra columna que necesite.</span><span class="sxs-lookup"><span data-stu-id="168af-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="168af-110">Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar un grupo de filas.</span><span class="sxs-lookup"><span data-stu-id="168af-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="168af-111">Hasta que ya no haya ninguna fila en la tabla de contenido:</span><span class="sxs-lookup"><span data-stu-id="168af-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="168af-112">Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir el mensaje representado por el identificador de entrada de cada fila.</span><span class="sxs-lookup"><span data-stu-id="168af-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="168af-113">Asigne el parámetro _lppUnk_ a un puntero de interfaz **IMessage** local.</span><span class="sxs-lookup"><span data-stu-id="168af-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="168af-114">Trabajar con las propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="168af-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="168af-115">Suelte el puntero al que apunta el parámetro _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="168af-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="168af-116">Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar el siguiente grupo de filas.</span><span class="sxs-lookup"><span data-stu-id="168af-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="168af-117">Suelte la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="168af-117">Release the contents table.</span></span>
    

