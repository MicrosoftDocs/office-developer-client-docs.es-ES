---
title: IFolderSupport IUnknown
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415778"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="beedd-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="beedd-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="beedd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="beedd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="beedd-105">Proporciona información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="beedd-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="beedd-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="beedd-106">Provided by:</span></span>  <br/> |<span data-ttu-id="beedd-107">Proveedor de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="beedd-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="beedd-108">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="beedd-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="beedd-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="beedd-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="beedd-110">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="beedd-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="beedd-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="beedd-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="beedd-112">Obtiene información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="beedd-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="beedd-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="beedd-113">Remarks</span></span>

<span data-ttu-id="beedd-114">Por lo general, Microsoft Office Outlook un proveedor de almacén MAPI para implementar esta interfaz si el proveedor desea compartir una carpeta.</span><span class="sxs-lookup"><span data-stu-id="beedd-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="beedd-115">La excepción es el Exchange Server de almacenamiento, que puede compartir carpetas sin implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="beedd-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="beedd-116">Un cliente puede consultar un **[IMAPIFolder](imapifolderimapicontainer.md)** para **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="beedd-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="beedd-117">Si esto se realiza correctamente, llame a **IFolderSupport::GetSupportMask** y compruebe si se **FS_SUPPORTS_SHARING** bit que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="beedd-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

