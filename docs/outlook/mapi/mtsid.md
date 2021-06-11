---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435176"
---
# <a name="mtsid"></a><span data-ttu-id="8486f-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="8486f-103">MTSID</span></span>

  
  
<span data-ttu-id="8486f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8486f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8486f-105">Contiene un identificador de entrada del sistema de transporte de mensajes (MTS) X.400.</span><span class="sxs-lookup"><span data-stu-id="8486f-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8486f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8486f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8486f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8486f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8486f-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="8486f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="8486f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="8486f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="8486f-110">Members</span><span class="sxs-lookup"><span data-stu-id="8486f-110">Members</span></span>

 <span data-ttu-id="8486f-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="8486f-111">**cb**</span></span>
  
> <span data-ttu-id="8486f-112">Recuento de bytes en la matriz descrita por el **miembro abEntry.**</span><span class="sxs-lookup"><span data-stu-id="8486f-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="8486f-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="8486f-113">**abEntry**</span></span>
  
> <span data-ttu-id="8486f-114">Matriz de bytes que contiene los datos del identificador de entrada de MTS.</span><span class="sxs-lookup"><span data-stu-id="8486f-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8486f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8486f-115">Remarks</span></span>

<span data-ttu-id="8486f-116">La **estructura MTSID** solo se usa para asignaciones X.400 de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="8486f-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="8486f-117">Corresponde a la estructura [DE MAPI FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="8486f-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="8486f-118">Un identificador MTS tiene el mismo formato que un identificador de entrada MAPI o un valor de propiedad binaria.</span><span class="sxs-lookup"><span data-stu-id="8486f-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="8486f-119">Los identificadores mts pueden ser especialmente útiles para cancelar mensajes diferidos.</span><span class="sxs-lookup"><span data-stu-id="8486f-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8486f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8486f-120">See also</span></span>



[<span data-ttu-id="8486f-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="8486f-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="8486f-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="8486f-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="8486f-123">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8486f-123">MAPI Structures</span></span>](mapi-structures.md)

