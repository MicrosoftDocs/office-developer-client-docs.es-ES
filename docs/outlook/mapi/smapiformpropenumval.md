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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578720"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="86f88-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="86f88-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="86f88-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86f88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86f88-105">Asigna un valor entero enumerado a un nombre para mostrar para ese valor.</span><span class="sxs-lookup"><span data-stu-id="86f88-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86f88-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="86f88-106">Header file:</span></span>  <br/> |<span data-ttu-id="86f88-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="86f88-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="86f88-108">Members</span><span class="sxs-lookup"><span data-stu-id="86f88-108">Members</span></span>

 <span data-ttu-id="86f88-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="86f88-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="86f88-110">Cadena que contiene el nombre para mostrar para el valor especificado en el miembro **nVal** .</span><span class="sxs-lookup"><span data-stu-id="86f88-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="86f88-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="86f88-111">**nVal**</span></span>
  
> <span data-ttu-id="86f88-112">Un valor de enumeración para el nombre para mostrar que señala el miembro **pszDisplayName** .</span><span class="sxs-lookup"><span data-stu-id="86f88-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86f88-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86f88-113">Remarks</span></span>

<span data-ttu-id="86f88-114">Cuando un usuario selecciona un nombre para mostrar de un formulario, se almacena valor de enumeración correspondiente del nombre mediante el uso de la implementación de la interfaz de [IMAPIProp](imapipropiunknown.md) que está asociada con el formulario.</span><span class="sxs-lookup"><span data-stu-id="86f88-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86f88-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="86f88-115">See also</span></span>



[<span data-ttu-id="86f88-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="86f88-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="86f88-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="86f88-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="86f88-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="86f88-118">MAPI Structures</span></span>](mapi-structures.md)

