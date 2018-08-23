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
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585685"
---
# <a name="mtsid"></a><span data-ttu-id="17c7e-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="17c7e-103">MTSID</span></span>

  
  
<span data-ttu-id="17c7e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17c7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17c7e-105">Contiene un identificador de entrada del sistema (MTS) de transporte de mensaje X.400.</span><span class="sxs-lookup"><span data-stu-id="17c7e-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17c7e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="17c7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="17c7e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17c7e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="17c7e-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="17c7e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="17c7e-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="17c7e-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="17c7e-110">Members</span><span class="sxs-lookup"><span data-stu-id="17c7e-110">Members</span></span>

 <span data-ttu-id="17c7e-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="17c7e-111">**cb**</span></span>
  
> <span data-ttu-id="17c7e-112">Número de bytes de la matriz descritos por el miembro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="17c7e-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="17c7e-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="17c7e-113">**abEntry**</span></span>
  
> <span data-ttu-id="17c7e-114">Matriz de bytes que contiene los datos del identificador de entrada MTS.</span><span class="sxs-lookup"><span data-stu-id="17c7e-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17c7e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17c7e-115">Remarks</span></span>

<span data-ttu-id="17c7e-116">La estructura **MTSID** se usa solo para X.400 asignaciones de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="17c7e-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="17c7e-117">Se corresponde con la estructura MAPI [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="17c7e-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="17c7e-118">Un identificador MTS tiene el mismo formato que un identificador de entrada MAPI o un valor de la propiedad binaria.</span><span class="sxs-lookup"><span data-stu-id="17c7e-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="17c7e-119">Los identificadores MTS pueden ser especialmente útiles para cancelar mensajes diferidos.</span><span class="sxs-lookup"><span data-stu-id="17c7e-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17c7e-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="17c7e-120">See also</span></span>



[<span data-ttu-id="17c7e-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="17c7e-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="17c7e-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="17c7e-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="17c7e-123">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="17c7e-123">MAPI Structures</span></span>](mapi-structures.md)

