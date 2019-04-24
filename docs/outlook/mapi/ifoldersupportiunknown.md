---
title: IUnknown A ifoldersupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351390"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="5e1a2-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e1a2-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="5e1a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e1a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e1a2-105">Proporciona información acerca de la compatibilidad de una carpeta con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5e1a2-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e1a2-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="5e1a2-106">Provided by:</span></span>  <br/> |<span data-ttu-id="5e1a2-107">Proveedor de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="5e1a2-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="5e1a2-108">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="5e1a2-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5e1a2-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="5e1a2-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5e1a2-110">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="5e1a2-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e1a2-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="5e1a2-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="5e1a2-112">Obtiene información sobre la compatibilidad de una carpeta con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5e1a2-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e1a2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e1a2-113">Remarks</span></span>

<span data-ttu-id="5e1a2-114">Por lo general, Microsoft Office Outlook requiere un proveedor de almacén MAPI para implementar esta interfaz si el proveedor desea compartir una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5e1a2-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="5e1a2-115">La excepción es el proveedor del almacén de Exchange Server, que puede compartir carpetas sin implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="5e1a2-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="5e1a2-116">Un cliente puede consultar un **[IMAPIFolder](imapifolderimapicontainer.md)** de **a ifoldersupport**.</span><span class="sxs-lookup"><span data-stu-id="5e1a2-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="5e1a2-117">Si se realiza correctamente, llame a **a ifoldersupport:: GetSupportMask** y compruebe el bit **FS_SUPPORTS_SHARING** que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="5e1a2-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

