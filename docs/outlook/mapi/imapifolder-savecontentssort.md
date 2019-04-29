---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411620"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="7c282-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="7c282-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="7c282-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c282-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c282-105">Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7c282-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7c282-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7c282-106">Parameters</span></span>

 <span data-ttu-id="7c282-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="7c282-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="7c282-108">a Un puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene el criterio de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7c282-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="7c282-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c282-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7c282-110">a Máscara de máscara de marcadores que controla cómo se establece el criterio de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7c282-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="7c282-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="7c282-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7c282-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="7c282-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="7c282-113">El valor predeterminado de criterio de ordenación se aplica a la carpeta indicada y a todas sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="7c282-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c282-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c282-114">Return value</span></span>

<span data-ttu-id="7c282-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c282-115">S_OK</span></span> 
  
> <span data-ttu-id="7c282-116">El criterio de ordenación se guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c282-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="7c282-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7c282-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7c282-118">El proveedor de almacenamiento de mensajes no admite guardar un criterio de ordenación para las tablas de contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7c282-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c282-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c282-119">Remarks</span></span>

<span data-ttu-id="7c282-120">El método **IMAPIFolder:: SaveContentsSort** establece un criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7c282-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="7c282-121">Es decir, cuando un cliente llama al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta después de que el código llama a **SaveContentsSort**, las filas de la tabla contenido devuelto aparecerán en el orden establecido por **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="7c282-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="7c282-122">No todos los proveedores de almacenamiento de mensajes admiten **SaveContentsSort**; es aceptable para los proveedores de almacenamiento de mensajes devolver MAPI_E_NO_SUPPORT desde el método **SaveContentsSort** .</span><span class="sxs-lookup"><span data-stu-id="7c282-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c282-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="7c282-123">See also</span></span>



[<span data-ttu-id="7c282-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="7c282-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="7c282-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="7c282-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="7c282-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7c282-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

