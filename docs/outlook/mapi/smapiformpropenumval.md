---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435414"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="960ba-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="960ba-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="960ba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="960ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="960ba-105">Asigna un valor entero enumerado a un nombre para mostrar para ese valor.</span><span class="sxs-lookup"><span data-stu-id="960ba-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="960ba-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="960ba-106">Header file:</span></span>  <br/> |<span data-ttu-id="960ba-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="960ba-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="960ba-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="960ba-108">Members</span></span>

 <span data-ttu-id="960ba-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="960ba-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="960ba-110">Cadena que contiene el nombre para mostrar del valor especificado en el **miembro nVal.**</span><span class="sxs-lookup"><span data-stu-id="960ba-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="960ba-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="960ba-111">**nVal**</span></span>
  
> <span data-ttu-id="960ba-112">Un valor de enumeración para el nombre para mostrar al que apunta el **miembro pszDisplayName.**</span><span class="sxs-lookup"><span data-stu-id="960ba-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="960ba-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="960ba-113">Remarks</span></span>

<span data-ttu-id="960ba-114">Cuando un usuario selecciona un nombre para mostrar de un formulario, el valor de enumeración correspondiente del nombre se almacena mediante la implementación de la interfaz [IMAPIProp](imapipropiunknown.md) asociada al formulario.</span><span class="sxs-lookup"><span data-stu-id="960ba-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="960ba-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="960ba-115">See also</span></span>



[<span data-ttu-id="960ba-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="960ba-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="960ba-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="960ba-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="960ba-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="960ba-118">MAPI Structures</span></span>](mapi-structures.md)

