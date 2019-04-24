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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336354"
---
# <a name="iid"></a><span data-ttu-id="966f7-103">IID</span><span class="sxs-lookup"><span data-stu-id="966f7-103">IID</span></span>

  
  
<span data-ttu-id="966f7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="966f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="966f7-105">Describe una estructura de [GUID](guid.md) que se usa para describir un identificador de una interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="966f7-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="966f7-106">Members</span><span class="sxs-lookup"><span data-stu-id="966f7-106">Members</span></span>

<span data-ttu-id="966f7-107">Consulte la estructura **GUID** .</span><span class="sxs-lookup"><span data-stu-id="966f7-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="966f7-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="966f7-108">Remarks</span></span>

<span data-ttu-id="966f7-109">Una estructura de **IID** se usa para identificar de forma exclusiva una interfaz MAPI y para asociar una interfaz determinada con un objeto.</span><span class="sxs-lookup"><span data-stu-id="966f7-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="966f7-110">Por ejemplo, cuando un cliente llama a [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir una carpeta, el cliente establece el parámetro _lpInterface_ para que apunte a un **IID** que representa la interfaz [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="966f7-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="966f7-111">MAPI define la **IMAPIFolderIID** para que sea IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="966f7-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="966f7-112">Las estructuras **IID** también se usan para identificar de forma exclusiva las interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="966f7-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="966f7-113">Todas las estructuras de **IID** específicas de las interfaces MAPI se definen en el archivo de encabezado Mapiguid. h.</span><span class="sxs-lookup"><span data-stu-id="966f7-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="966f7-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="966f7-114">See also</span></span>



[<span data-ttu-id="966f7-115">GUID</span><span class="sxs-lookup"><span data-stu-id="966f7-115">GUID</span></span>](guid.md)


[<span data-ttu-id="966f7-116">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="966f7-116">MAPI Structures</span></span>](mapi-structures.md)

