---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2af9d529cb92e1040427eba69270908dcf4a5d9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816688"
---
# <a name="direntryid"></a><span data-ttu-id="d1d3e-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d1d3e-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="d1d3e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1d3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1d3e-105">Se describen las propiedades de un identificador de entrada de Active directory.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1d3e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d1d3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1d3e-107">EntryID.h</span><span class="sxs-lookup"><span data-stu-id="d1d3e-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d1d3e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1d3e-108">Members</span></span>

 <span data-ttu-id="d1d3e-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-109">**abFlags**</span></span>
  
> <span data-ttu-id="d1d3e-110">Una máscara de bits de indicadores que proporciona información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="d1d3e-111">Para obtener más información, vea la descripción del campo **abFlags** de una estructura de [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d3e-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="d1d3e-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-112">**muid**</span></span>
  
> <span data-ttu-id="d1d3e-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="d1d3e-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-114">**ulVersion**</span></span>
  
> <span data-ttu-id="d1d3e-115">El número de versión de la estructura **DIR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="d1d3e-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="d1d3e-116">Debe establecerse en CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="d1d3e-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-117">**ulType**</span></span>
  
> <span data-ttu-id="d1d3e-118">Un entero que representa el tipo de identificador de entrada de Active directory.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="d1d3e-119">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d1d3e-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="d1d3e-120">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-120">**Name**</span></span>|<span data-ttu-id="d1d3e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1d3e-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="d1d3e-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="d1d3e-123">La carpeta raíz de una libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="d1d3e-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="d1d3e-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="d1d3e-125">Una subcarpeta dentro de la carpeta raíz del objeto de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="d1d3e-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="d1d3e-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="d1d3e-127">Un objeto de contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="d1d3e-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="d1d3e-128">**muidID**</span></span>
  
> <span data-ttu-id="d1d3e-129">Un GUID que identifica el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1d3e-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d1d3e-130">Remarks</span></span>

<span data-ttu-id="d1d3e-131">Las estructuras de **DIR_ENTRYID** y [CONTAB_ENTRYID](contab_entryid.md) son idénticas, excepto por el miembro **ulType** .</span><span class="sxs-lookup"><span data-stu-id="d1d3e-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="d1d3e-132">El contenido del miembro **ulType** determina qué estructura es apropiada para los campos restantes.</span><span class="sxs-lookup"><span data-stu-id="d1d3e-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1d3e-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="d1d3e-133">See also</span></span>



[<span data-ttu-id="d1d3e-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d1d3e-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="d1d3e-135">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d1d3e-135">MAPI Structures</span></span>](mapi-structures.md)

