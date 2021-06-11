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
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416702"
---
# <a name="smapiformprop"></a><span data-ttu-id="6b229-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="6b229-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="6b229-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b229-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b229-105">Describe una propiedad con nombre usada con un formulario.</span><span class="sxs-lookup"><span data-stu-id="6b229-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b229-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6b229-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b229-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="6b229-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="6b229-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b229-108">Members</span></span>

 <span data-ttu-id="6b229-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6b229-109">**ulFlags**</span></span>
  
> <span data-ttu-id="6b229-110">Marcas usadas para distinguir el formato de las cadenas de la **estructura SMAPIFormProp.**</span><span class="sxs-lookup"><span data-stu-id="6b229-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="6b229-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="6b229-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="6b229-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6b229-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6b229-113">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6b229-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="6b229-114">Si MAPI_UNICODE no está establecido, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6b229-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6b229-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="6b229-115">**nPropType**</span></span>
  
> <span data-ttu-id="6b229-116">Tipo de la propiedad con nombre, con la palabra más significativa establecida en cero.</span><span class="sxs-lookup"><span data-stu-id="6b229-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="6b229-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="6b229-117">**nmid**</span></span>
  
> <span data-ttu-id="6b229-118">Nombre de la propiedad con nombre, que incluye una estructura **GUID** que identifica el conjunto de propiedades y un valor numérico o de cadena que representa un identificador de interfaz y un nombre de formulario.</span><span class="sxs-lookup"><span data-stu-id="6b229-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="6b229-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="6b229-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="6b229-120">Puntero al nombre para mostrar de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="6b229-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="6b229-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="6b229-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="6b229-122">Valor que describe el tipo de datos incluidos en el **miembro u.**</span><span class="sxs-lookup"><span data-stu-id="6b229-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="6b229-123">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b229-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="6b229-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="6b229-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="6b229-125">El **miembro u** no contiene una enumeración.</span><span class="sxs-lookup"><span data-stu-id="6b229-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="6b229-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="6b229-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="6b229-127">El **miembro u** contiene una estructura que describe una enumeración.</span><span class="sxs-lookup"><span data-stu-id="6b229-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="6b229-128">**s**</span><span class="sxs-lookup"><span data-stu-id="6b229-128">**u**</span></span>
  
> <span data-ttu-id="6b229-129">Union que describe la asociación entre el nombre y el número de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="6b229-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="6b229-130">Al usar algunas propiedades, el **miembro u** está vacío.</span><span class="sxs-lookup"><span data-stu-id="6b229-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="6b229-131">Con otras propiedades, se representa en una estructura formada por los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="6b229-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="6b229-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="6b229-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="6b229-133">Estructura [MAPINAMEID](mapinameid.md) que contiene el conjunto de propiedades y el identificador de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="6b229-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="6b229-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="6b229-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="6b229-135">Recuento de [estructuras SMAPIFormPropEnumVal](smapiformpropenumval.md) en la matriz señalada por el **miembro pfpevAvailable.**</span><span class="sxs-lookup"><span data-stu-id="6b229-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="6b229-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="6b229-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="6b229-137">Puntero a una matriz **de estructuras SMAPIFormPropEnumVal,** cada una de las cuales contiene un valor para la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="6b229-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b229-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b229-138">Remarks</span></span>

<span data-ttu-id="6b229-139">La **estructura SMAPIFormProp** contiene información sobre una propiedad de formulario usada como parte de las definiciones de la [interfaz IMAPIFormInfo;](imapiforminfoimapiprop.md) **nSpecialType** contiene una etiqueta que se aplica a la **unión u** que forma parte de **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="6b229-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b229-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b229-140">See also</span></span>



[<span data-ttu-id="6b229-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="6b229-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="6b229-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="6b229-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="6b229-143">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="6b229-143">MAPI Structures</span></span>](mapi-structures.md)

