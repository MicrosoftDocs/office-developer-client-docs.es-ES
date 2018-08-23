---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b1b037cf24c1bb5a0c84da3d59892ab15763f37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588247"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="99ef0-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="99ef0-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="99ef0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99ef0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99ef0-105">Proporciona acceso a la tabla de perfil, una tabla que contiene información acerca de todos los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="99ef0-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="99ef0-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="99ef0-106">Parameters</span></span>

 <span data-ttu-id="99ef0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99ef0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="99ef0-108">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="99ef0-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="99ef0-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="99ef0-109">_lppTable_</span></span>
  
> <span data-ttu-id="99ef0-110">[out] Un puntero a un puntero a la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="99ef0-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99ef0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99ef0-111">Return value</span></span>

<span data-ttu-id="99ef0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="99ef0-112">S_OK</span></span> 
  
> <span data-ttu-id="99ef0-113">La tabla de perfil se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99ef0-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99ef0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99ef0-114">Remarks</span></span>

<span data-ttu-id="99ef0-115">El método **IProfAdmin::GetProfileTable** proporciona acceso a la tabla de perfil, que contiene una fila por cada perfil disponible.</span><span class="sxs-lookup"><span data-stu-id="99ef0-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="99ef0-116">Hay sólo dos columnas de cada fila: nombre para mostrar del perfil y una marca que indica si el perfil es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="99ef0-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="99ef0-117">Los perfiles que se han eliminado, o que están en uso pero que se han marcado para su eliminación, no se incluyen en la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="99ef0-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="99ef0-118">La tabla de perfil es estática; subsiguientes adiciones y eliminaciones de perfiles no se reflejan en la tabla.</span><span class="sxs-lookup"><span data-stu-id="99ef0-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="99ef0-119">Si no hay perfiles existen, **GetProfileTable** devuelve un objeto table con cero filas.</span><span class="sxs-lookup"><span data-stu-id="99ef0-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="99ef0-120">Para obtener más información acerca de la tabla de perfil, vea [Las tablas de perfil](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="99ef0-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="99ef0-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="99ef0-121">MFCMAPI reference</span></span>

<span data-ttu-id="99ef0-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="99ef0-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="99ef0-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="99ef0-123">**File**</span></span>|<span data-ttu-id="99ef0-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="99ef0-124">**Function**</span></span>|<span data-ttu-id="99ef0-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="99ef0-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99ef0-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="99ef0-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="99ef0-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="99ef0-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="99ef0-128">MFCMAPI usa el método **IProfAdmin::GetProfileTable** para obtener la tabla de perfil para mostrar un cuadro de diálogo nuevo.</span><span class="sxs-lookup"><span data-stu-id="99ef0-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99ef0-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="99ef0-129">See also</span></span>



[<span data-ttu-id="99ef0-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99ef0-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="99ef0-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="99ef0-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="99ef0-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99ef0-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="99ef0-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="99ef0-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

