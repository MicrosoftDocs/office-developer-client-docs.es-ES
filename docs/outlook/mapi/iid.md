---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411599"
---
# <a name="iid"></a><span data-ttu-id="e43c7-103">IID</span><span class="sxs-lookup"><span data-stu-id="e43c7-103">IID</span></span>

  
  
<span data-ttu-id="e43c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e43c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e43c7-105">Describe una [estructura GUID](guid.md) usada para describir un identificador para una interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="e43c7-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="e43c7-106">Members</span><span class="sxs-lookup"><span data-stu-id="e43c7-106">Members</span></span>

<span data-ttu-id="e43c7-107">Vea la **estructura GUID.**</span><span class="sxs-lookup"><span data-stu-id="e43c7-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e43c7-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e43c7-108">Remarks</span></span>

<span data-ttu-id="e43c7-109">Una **estructura IID** se usa para identificar de forma única una interfaz MAPI y asociar una interfaz determinada con un objeto.</span><span class="sxs-lookup"><span data-stu-id="e43c7-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="e43c7-110">Por ejemplo, cuando un cliente llama a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir una carpeta, el cliente establece el parámetro _lpInterface_ para que apunte a un **IID** que representa la [interfaz IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="e43c7-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="e43c7-111">MAPI define el **IMAPIFolderIID para** que se IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="e43c7-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="e43c7-112">**Las estructuras IID** también se usan para identificar de forma única interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="e43c7-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="e43c7-113">Todas las estructuras **de IID** específicas para las interfaces MAPI se definen en el archivo de encabezado Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="e43c7-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e43c7-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="e43c7-114">See also</span></span>



[<span data-ttu-id="e43c7-115">GUID</span><span class="sxs-lookup"><span data-stu-id="e43c7-115">GUID</span></span>](guid.md)


[<span data-ttu-id="e43c7-116">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e43c7-116">MAPI Structures</span></span>](mapi-structures.md)

