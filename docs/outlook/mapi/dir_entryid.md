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
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316677"
---
# <a name="direntryid"></a><span data-ttu-id="4ea0f-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4ea0f-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="4ea0f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ea0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ea0f-105">Describe las propiedades de un identificador de entrada de directorio.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ea0f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4ea0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4ea0f-107">EntryID. h</span><span class="sxs-lookup"><span data-stu-id="4ea0f-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="4ea0f-108">Members</span><span class="sxs-lookup"><span data-stu-id="4ea0f-108">Members</span></span>

 <span data-ttu-id="4ea0f-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-109">**abFlags**</span></span>
  
> <span data-ttu-id="4ea0f-110">Máscara de máscara de marcadores que proporciona información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="4ea0f-111">Para obtener más información, vea la descripción del campo **abFlags** de una estructura [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="4ea0f-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="4ea0f-112">**Muid**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-112">**muid**</span></span>
  
> <span data-ttu-id="4ea0f-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="4ea0f-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-114">**ulVersion**</span></span>
  
> <span data-ttu-id="4ea0f-115">Número de versión de la estructura **DIR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="4ea0f-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="4ea0f-116">Debe establecerse en CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="4ea0f-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-117">**ulType**</span></span>
  
> <span data-ttu-id="4ea0f-118">Entero que representa el tipo de identificador de entrada de directorio.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="4ea0f-119">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="4ea0f-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="4ea0f-120">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-120">**Name**</span></span>|<span data-ttu-id="4ea0f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ea0f-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="4ea0f-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="4ea0f-123">La carpeta raíz de una libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="4ea0f-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="4ea0f-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="4ea0f-125">Una subcarpeta incluida en la carpeta raíz del objeto de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="4ea0f-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="4ea0f-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="4ea0f-127">Un objeto contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="4ea0f-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="4ea0f-128">**muidID**</span></span>
  
> <span data-ttu-id="4ea0f-129">GUID que identifica el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ea0f-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ea0f-130">Remarks</span></span>

<span data-ttu-id="4ea0f-131">Las estructuras **DIR_ENTRYID** y [CONTAB_ENTRYID](contab_entryid.md) son idénticas, excepto para el miembro **ulType** .</span><span class="sxs-lookup"><span data-stu-id="4ea0f-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="4ea0f-132">El contenido del miembro **ulType** determina qué estructura es adecuada para los campos restantes.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ea0f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ea0f-133">See also</span></span>



[<span data-ttu-id="4ea0f-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4ea0f-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="4ea0f-135">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="4ea0f-135">MAPI Structures</span></span>](mapi-structures.md)

