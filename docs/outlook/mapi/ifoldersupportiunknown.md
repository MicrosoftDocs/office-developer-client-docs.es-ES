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
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564174"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="53a12-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53a12-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="53a12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53a12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53a12-105">Proporciona información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="53a12-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53a12-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="53a12-106">Provided by:</span></span>  <br/> |<span data-ttu-id="53a12-107">Proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="53a12-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="53a12-108">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="53a12-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="53a12-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="53a12-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="53a12-110">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="53a12-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53a12-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="53a12-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="53a12-112">Obtiene información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="53a12-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53a12-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53a12-113">Remarks</span></span>

<span data-ttu-id="53a12-114">Por lo general, Microsoft Office Outlook requiere una MAPI proveedor para implementar esta interfaz si desea que el proveedor compartir una carpeta de almacén.</span><span class="sxs-lookup"><span data-stu-id="53a12-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="53a12-115">La excepción es el proveedor de almacén de Exchange Server, que puede compartir carpetas sin tener que implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="53a12-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="53a12-116">Un cliente puede consultar un **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="53a12-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="53a12-117">Si se realiza correctamente, llame a **IFolderSupport::GetSupportMask** y compruebe si el bit **FS_SUPPORTS_SHARING** va a establecer.</span><span class="sxs-lookup"><span data-stu-id="53a12-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

