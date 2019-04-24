---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339385"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="53375-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="53375-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="53375-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53375-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53375-105">Quita una o más entradas, normalmente usuarios de mensajería, listas de distribución u otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="53375-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="53375-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="53375-106">Parameters</span></span>

 <span data-ttu-id="53375-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="53375-107">_lpEntries_</span></span>
  
> <span data-ttu-id="53375-108">a Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que contiene los identificadores de entrada que representan las entradas que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="53375-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="53375-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53375-109">_ulFlags_</span></span>
  
> <span data-ttu-id="53375-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53375-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53375-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53375-111">Return value</span></span>

<span data-ttu-id="53375-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="53375-112">S_OK</span></span> 
  
> <span data-ttu-id="53375-113">Las entradas especificadas se han eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="53375-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="53375-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="53375-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="53375-115">La llamada se realizó correctamente, pero no se pudo eliminar una o varias de las entradas.</span><span class="sxs-lookup"><span data-stu-id="53375-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="53375-116">Cuando se devuelve este valor, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="53375-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="53375-117">Para comprobar este valor, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="53375-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="53375-118">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="53375-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="53375-119">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="53375-119">MFCMAPI reference</span></span>

<span data-ttu-id="53375-120">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="53375-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53375-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="53375-121">**File**</span></span>|<span data-ttu-id="53375-122">**Función**</span><span class="sxs-lookup"><span data-stu-id="53375-122">**Function**</span></span>|<span data-ttu-id="53375-123">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="53375-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53375-124">Abdlg. cpp</span><span class="sxs-lookup"><span data-stu-id="53375-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="53375-125">CabDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="53375-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="53375-126">MFCMAPI usa el método **DeleteEntries** para eliminar una entrada específica de un contenedor de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="53375-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53375-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="53375-127">See also</span></span>



[<span data-ttu-id="53375-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="53375-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="53375-129">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="53375-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

