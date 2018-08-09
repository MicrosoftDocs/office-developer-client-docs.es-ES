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
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817188"
---
# <a name="iid"></a><span data-ttu-id="8cc05-103">IID</span><span class="sxs-lookup"><span data-stu-id="8cc05-103">IID</span></span>

  
  
<span data-ttu-id="8cc05-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cc05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cc05-105">Describe una estructura [GUID](guid.md) que se usa para describir un identificador para una interfaz de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8cc05-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="8cc05-106">Members</span><span class="sxs-lookup"><span data-stu-id="8cc05-106">Members</span></span>

<span data-ttu-id="8cc05-107">Ver la estructura **GUID** .</span><span class="sxs-lookup"><span data-stu-id="8cc05-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8cc05-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cc05-108">Remarks</span></span>

<span data-ttu-id="8cc05-109">Una estructura de **IID** se usa para identificar de forma exclusiva una interfaz de MAPI y para asociar una interfaz determinada a un objeto.</span><span class="sxs-lookup"><span data-stu-id="8cc05-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="8cc05-110">Por ejemplo, cuando un cliente llama a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir una carpeta, el cliente establece el parámetro _lpInterface_ para que apunte a un **IID** que representa la interfaz [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc05-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="8cc05-111">MAPI define la **IMAPIFolderIID** para que sea IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="8cc05-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="8cc05-112">**IID** estructuras también se usan para identificar de forma exclusiva interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="8cc05-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="8cc05-113">Todas las estructuras **IID** específicas para las interfaces MAPI se definen en el archivo de encabezado Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="8cc05-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8cc05-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cc05-114">See also</span></span>



[<span data-ttu-id="8cc05-115">GUID</span><span class="sxs-lookup"><span data-stu-id="8cc05-115">GUID</span></span>](guid.md)


[<span data-ttu-id="8cc05-116">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8cc05-116">MAPI Structures</span></span>](mapi-structures.md)

