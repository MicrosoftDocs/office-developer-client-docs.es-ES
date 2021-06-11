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
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414650"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="a0ae7-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="a0ae7-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="a0ae7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0ae7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0ae7-105">Proporciona acceso a la tabla de perfiles, una tabla que contiene información sobre todos los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="a0ae7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0ae7-106">Parameters</span></span>

 <span data-ttu-id="a0ae7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0ae7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a0ae7-108">[in] Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="a0ae7-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a0ae7-109">_lppTable_</span></span>
  
> <span data-ttu-id="a0ae7-110">[salida] Puntero a un puntero a la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0ae7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0ae7-111">Return value</span></span>

<span data-ttu-id="a0ae7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0ae7-112">S_OK</span></span> 
  
> <span data-ttu-id="a0ae7-113">La tabla de perfiles se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0ae7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0ae7-114">Remarks</span></span>

<span data-ttu-id="a0ae7-115">El **método IProfAdmin::GetProfileTable** proporciona acceso a la tabla de perfiles, que contiene una fila por cada perfil disponible.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="a0ae7-116">Solo hay dos columnas en cada fila: el nombre para mostrar del perfil y una marca que indica si el perfil es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="a0ae7-117">Los perfiles que se han eliminado o que están en uso pero que se han marcado para su eliminación, no se incluyen en la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="a0ae7-118">La tabla de perfiles es estática; Las adiciones y eliminaciones posteriores de perfiles no se reflejan en la tabla.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="a0ae7-119">Si no existen perfiles, **GetProfileTable** devuelve una tabla con cero filas.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="a0ae7-120">Para obtener más información acerca de la tabla de perfiles, vea [Tablas de perfiles](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a0ae7-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a0ae7-121">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a0ae7-121">MFCMAPI reference</span></span>

<span data-ttu-id="a0ae7-122">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a0ae7-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a0ae7-123">**File**</span></span>|<span data-ttu-id="a0ae7-124">**Función**</span><span class="sxs-lookup"><span data-stu-id="a0ae7-124">**Function**</span></span>|<span data-ttu-id="a0ae7-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a0ae7-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0ae7-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a0ae7-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a0ae7-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="a0ae7-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="a0ae7-128">MFCMAPI usa el **método IProfAdmin::GetProfileTable** para que la tabla de perfiles se muestre en un nuevo cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a0ae7-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0ae7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0ae7-129">See also</span></span>



[<span data-ttu-id="a0ae7-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0ae7-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="a0ae7-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="a0ae7-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="a0ae7-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0ae7-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="a0ae7-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a0ae7-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

