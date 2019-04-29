---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407245"
---
# <a name="flatentry"></a><span data-ttu-id="bd2d8-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="bd2d8-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="bd2d8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd2d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd2d8-105">Una estructura [EntryID](entryid.md) más un recuento de bytes que especifica el tamaño de la estructura **EntryID** .</span><span class="sxs-lookup"><span data-stu-id="bd2d8-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd2d8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bd2d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd2d8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bd2d8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bd2d8-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="bd2d8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="bd2d8-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="bd2d8-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="bd2d8-110">Members</span><span class="sxs-lookup"><span data-stu-id="bd2d8-110">Members</span></span>

 <span data-ttu-id="bd2d8-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="bd2d8-111">**cb**</span></span>
  
> <span data-ttu-id="bd2d8-112">Número de bytes en el miembro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="bd2d8-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="bd2d8-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="bd2d8-113">**abEntry**</span></span>
  
> <span data-ttu-id="bd2d8-114">Identificador de entrada completo que incluye la matriz de marcadores y datos binarios.</span><span class="sxs-lookup"><span data-stu-id="bd2d8-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd2d8-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd2d8-115">Remarks</span></span>

<span data-ttu-id="bd2d8-116">Una estructura **FLATENTRY** es similar A una estructura [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2d8-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="bd2d8-117">Sin embargo, hay algunas diferencias:</span><span class="sxs-lookup"><span data-stu-id="bd2d8-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="bd2d8-118">Una estructura **FLATENTRY** almacena el tamaño del identificador de entrada; **EntryID** no.</span><span class="sxs-lookup"><span data-stu-id="bd2d8-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="bd2d8-119">Una estructura **FLATENTRY** almacena los datos de la marca junto con el resto del identificador de entrada; **EntryID** los almacena por separado.</span><span class="sxs-lookup"><span data-stu-id="bd2d8-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="bd2d8-120">Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes mientras que los métodos de la interfaz [IMAPIProp](imapipropiunknown.md) usan la estructura **EntryID** y los métodos **OpenEntry** siguientes: [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [IMAPISupport:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [IMSLogon:: OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="bd2d8-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="bd2d8-121">Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="bd2d8-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="bd2d8-122">Se usa una estructura **EntryID** para almacenar un identificador de entrada en el disco.</span><span class="sxs-lookup"><span data-stu-id="bd2d8-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bd2d8-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="bd2d8-123">See also</span></span>



[<span data-ttu-id="bd2d8-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bd2d8-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="bd2d8-125">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="bd2d8-125">MAPI Structures</span></span>](mapi-structures.md)

