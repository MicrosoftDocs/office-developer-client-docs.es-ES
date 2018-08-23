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
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594491"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="1dbf3-103">Recorrer la carpeta Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="1dbf3-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="1dbf3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dbf3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="1dbf3-105">**Para desplazarse por todos los mensajes en la Bandeja de entrada**</span><span class="sxs-lookup"><span data-stu-id="1dbf3-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="1dbf3-106">Llame a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar el identificador de entrada de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="1dbf3-107">Llame a **IMAPIFolder::OpenEntry** para abrir la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="1dbf3-108">Llamar al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la Bandeja de entrada para recuperar la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="1dbf3-109">Llamar el contenido [IMAPITable::SetColumns](imapitable-setcolumns.md) al método de la tabla para limitar la columna establecida en la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y todas las columnas que necesite.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="1dbf3-110">Llamar a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar un grupo de filas.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="1dbf3-111">Hasta que ya no hay ninguna fila en la tabla de contenido:</span><span class="sxs-lookup"><span data-stu-id="1dbf3-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="1dbf3-112">Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir el mensaje representado por el identificador de entrada de cada fila.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="1dbf3-113">Asigne el parámetro _lppUnk_ a un puntero de interfaz **IMessage** local.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="1dbf3-114">Trabajar con las propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="1dbf3-115">Liberar el puntero que señala el parámetro _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="1dbf3-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="1dbf3-116">Llamar a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar el siguiente grupo de filas.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="1dbf3-117">Versión en la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-117">Release the contents table.</span></span>
    

