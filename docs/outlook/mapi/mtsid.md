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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818419"
---
# <a name="mtsid"></a><span data-ttu-id="a8cbf-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="a8cbf-103">MTSID</span></span>

  
  
<span data-ttu-id="a8cbf-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8cbf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8cbf-105">Contiene un identificador de entrada del sistema (MTS) de transporte de mensaje X.400.</span><span class="sxs-lookup"><span data-stu-id="a8cbf-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8cbf-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a8cbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8cbf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8cbf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a8cbf-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="a8cbf-108">Related macros:</span></span>  <br/> |<span data-ttu-id="a8cbf-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="a8cbf-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="a8cbf-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8cbf-110">Members</span></span>

 <span data-ttu-id="a8cbf-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="a8cbf-111">**cb**</span></span>
  
> <span data-ttu-id="a8cbf-112">Número de bytes de la matriz descritos por el miembro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="a8cbf-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="a8cbf-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="a8cbf-113">**abEntry**</span></span>
  
> <span data-ttu-id="a8cbf-114">Matriz de bytes que contiene los datos del identificador de entrada MTS.</span><span class="sxs-lookup"><span data-stu-id="a8cbf-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8cbf-115">Notas</span><span class="sxs-lookup"><span data-stu-id="a8cbf-115">Remarks</span></span>

<span data-ttu-id="a8cbf-116">La estructura **MTSID** se usa solo para X.400 asignaciones de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8cbf-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="a8cbf-117">Se corresponde con la estructura MAPI [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="a8cbf-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="a8cbf-118">Un identificador MTS tiene el mismo formato que un identificador de entrada MAPI o un valor de la propiedad binaria.</span><span class="sxs-lookup"><span data-stu-id="a8cbf-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="a8cbf-119">Los identificadores MTS pueden ser especialmente útiles para cancelar mensajes diferidos.</span><span class="sxs-lookup"><span data-stu-id="a8cbf-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8cbf-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="a8cbf-120">See also</span></span>



[<span data-ttu-id="a8cbf-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="a8cbf-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="a8cbf-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="a8cbf-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="a8cbf-123">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a8cbf-123">MAPI Structures</span></span>](mapi-structures.md)

