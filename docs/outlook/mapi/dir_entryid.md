---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583347"
---
# <a name="direntryid"></a><span data-ttu-id="f2446-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f2446-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="f2446-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2446-105">Se describen las propiedades de un identificador de entrada de Active directory.</span><span class="sxs-lookup"><span data-stu-id="f2446-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2446-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f2446-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2446-107">EntryID.h</span><span class="sxs-lookup"><span data-stu-id="f2446-107">entryid.h</span></span>  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a><span data-ttu-id="f2446-108">Members</span><span class="sxs-lookup"><span data-stu-id="f2446-108">Members</span></span>

 <span data-ttu-id="f2446-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="f2446-109">**abFlags**</span></span>
  
> <span data-ttu-id="f2446-110">Una máscara de bits de indicadores que proporciona información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="f2446-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="f2446-111">Para obtener más información, vea la descripción del campo **abFlags** de una estructura de [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="f2446-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="f2446-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="f2446-112">**muid**</span></span>
  
> <span data-ttu-id="f2446-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="f2446-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="f2446-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="f2446-114">**ulVersion**</span></span>
  
> <span data-ttu-id="f2446-115">El número de versión de la estructura **DIR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="f2446-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="f2446-116">Debe establecerse en CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="f2446-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="f2446-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="f2446-117">**ulType**</span></span>
  
> <span data-ttu-id="f2446-118">Un entero que representa el tipo de identificador de entrada de Active directory.</span><span class="sxs-lookup"><span data-stu-id="f2446-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="f2446-119">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f2446-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="f2446-120">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f2446-120">**Name**</span></span>|<span data-ttu-id="f2446-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2446-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2446-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="f2446-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="f2446-123">La carpeta raíz de una libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="f2446-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="f2446-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="f2446-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="f2446-125">Una subcarpeta dentro de la carpeta raíz del objeto de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="f2446-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="f2446-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="f2446-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="f2446-127">Un objeto de contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f2446-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="f2446-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="f2446-128">**muidID**</span></span>
  
> <span data-ttu-id="f2446-129">Un GUID que identifica el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="f2446-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2446-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2446-130">Remarks</span></span>

<span data-ttu-id="f2446-131">Las estructuras de **DIR_ENTRYID** y [CONTAB_ENTRYID](contab_entryid.md) son idénticas, excepto por el miembro **ulType** .</span><span class="sxs-lookup"><span data-stu-id="f2446-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="f2446-132">El contenido del miembro **ulType** determina qué estructura es apropiada para los campos restantes.</span><span class="sxs-lookup"><span data-stu-id="f2446-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2446-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f2446-133">See also</span></span>



[<span data-ttu-id="f2446-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f2446-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="f2446-135">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f2446-135">MAPI Structures</span></span>](mapi-structures.md)

