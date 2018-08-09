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
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817246"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="0b79a-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="0b79a-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="0b79a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b79a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b79a-105">Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0b79a-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0b79a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b79a-106">Parameters</span></span>

 <span data-ttu-id="0b79a-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="0b79a-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="0b79a-108">[entrada] Un puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene el criterio de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0b79a-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="0b79a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0b79a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0b79a-110">[entrada] Una máscara de bits de indicadores que controla cómo se establece el criterio de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0b79a-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="0b79a-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="0b79a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0b79a-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="0b79a-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="0b79a-113">El conjunto de criterio de ordenación predeterminado se aplica a la carpeta indicada y a todas sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="0b79a-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b79a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b79a-114">Return value</span></span>

<span data-ttu-id="0b79a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b79a-115">S_OK</span></span> 
  
> <span data-ttu-id="0b79a-116">El criterio de ordenación se guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b79a-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="0b79a-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0b79a-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0b79a-118">El proveedor de almacén de mensajes no admite guardar un criterio de ordenación para sus tablas de contenido de carpeta.</span><span class="sxs-lookup"><span data-stu-id="0b79a-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b79a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b79a-119">Remarks</span></span>

<span data-ttu-id="0b79a-120">El método **IMAPIFolder::SaveContentsSort** establece un criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0b79a-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="0b79a-121">Es decir, cuando un cliente llama (método) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta después de las llamadas de código **SaveContentsSort**, las filas de la tabla de contenido devuelto se muestra en el orden establecido por **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="0b79a-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="0b79a-122">No todos los proveedores de almacén de mensajes admiten **SaveContentsSort**; es aceptable para los proveedores de almacén de mensajes devolver MAPI_E_NO_SUPPORT desde el método **SaveContentsSort** .</span><span class="sxs-lookup"><span data-stu-id="0b79a-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b79a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b79a-123">See also</span></span>



[<span data-ttu-id="0b79a-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="0b79a-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="0b79a-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0b79a-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="0b79a-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0b79a-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

