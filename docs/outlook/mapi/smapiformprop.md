---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4e8e2474d2adb882dd0ba43aeb0d8b05044a6ce6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592062"
---
# <a name="smapiformprop"></a><span data-ttu-id="72a18-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="72a18-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="72a18-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72a18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72a18-105">Describe una propiedad con nombre que se utiliza con un formulario.</span><span class="sxs-lookup"><span data-stu-id="72a18-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72a18-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="72a18-106">Header file:</span></span>  <br/> |<span data-ttu-id="72a18-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="72a18-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a><span data-ttu-id="72a18-108">Members</span><span class="sxs-lookup"><span data-stu-id="72a18-108">Members</span></span>

 <span data-ttu-id="72a18-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="72a18-109">**ulFlags**</span></span>
  
> <span data-ttu-id="72a18-110">Marcas que se usan para distinguir el formato de las cadenas de la estructura de **SMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="72a18-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="72a18-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="72a18-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="72a18-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="72a18-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="72a18-113">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="72a18-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="72a18-114">Si no se establece MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="72a18-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="72a18-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="72a18-115">**nPropType**</span></span>
  
> <span data-ttu-id="72a18-116">Tipo de la propiedad con nombre, con la palabra más importante que se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="72a18-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="72a18-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="72a18-117">**nmid**</span></span>
  
> <span data-ttu-id="72a18-118">Nombre de la propiedad con nombre, que incluye una estructura **GUID** que identifica el valor de propiedad set y una numérica o de cadena que representa un nombre de identificador y el formulario de interfaz.</span><span class="sxs-lookup"><span data-stu-id="72a18-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="72a18-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="72a18-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="72a18-120">Puntero en el nombre para mostrar de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="72a18-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="72a18-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="72a18-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="72a18-122">Valor que describe el tipo de datos incluidos en el miembro **u** .</span><span class="sxs-lookup"><span data-stu-id="72a18-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="72a18-123">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="72a18-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="72a18-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="72a18-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="72a18-125">El miembro **u** no contiene una enumeración.</span><span class="sxs-lookup"><span data-stu-id="72a18-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="72a18-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="72a18-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="72a18-127">El miembro **u** contiene una estructura que describe una enumeración.</span><span class="sxs-lookup"><span data-stu-id="72a18-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="72a18-128">**s**</span><span class="sxs-lookup"><span data-stu-id="72a18-128">**u**</span></span>
  
> <span data-ttu-id="72a18-129">Unión que describe la asociación entre el nombre y el número de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="72a18-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="72a18-130">Mediante el uso de algunas propiedades, el miembro **u** está vacío.</span><span class="sxs-lookup"><span data-stu-id="72a18-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="72a18-131">Con otras propiedades, se representa en una estructura que consta de los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="72a18-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="72a18-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="72a18-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="72a18-133">La estructura [MAPINAMEID](mapinameid.md) que contiene el conjunto de propiedades y el identificador de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="72a18-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="72a18-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="72a18-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="72a18-135">Recuento de las estructuras de [SMAPIFormPropEnumVal](smapiformpropenumval.md) en la matriz indicada por el miembro **pfpevAvailable** .</span><span class="sxs-lookup"><span data-stu-id="72a18-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="72a18-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="72a18-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="72a18-137">Puntero a una matriz de estructuras **SMAPIFormPropEnumVal** , cada uno de los cuales contiene un valor para la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="72a18-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="72a18-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72a18-138">Remarks</span></span>

<span data-ttu-id="72a18-139">La estructura **SMAPIFormProp** contiene información sobre una propiedad de formulario que se usa como parte de las definiciones de la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) . **nSpecialType** contiene una etiqueta que se aplica a la unión **u** que forma parte de **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="72a18-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72a18-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="72a18-140">See also</span></span>



[<span data-ttu-id="72a18-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="72a18-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="72a18-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="72a18-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="72a18-143">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="72a18-143">MAPI Structures</span></span>](mapi-structures.md)

