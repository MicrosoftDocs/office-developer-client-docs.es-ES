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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c744407790fecde6b6d89dff669ea4db07ce7701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817084"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="8eda6-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="8eda6-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="8eda6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8eda6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8eda6-105">Quita una o más entradas, normalmente otros contenedores, listas de distribución o a los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="8eda6-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8eda6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8eda6-106">Parameters</span></span>

 <span data-ttu-id="8eda6-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="8eda6-107">_lpEntries_</span></span>
  
> <span data-ttu-id="8eda6-108">[entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que contienen los identificadores de entrada que representan las entradas que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8eda6-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="8eda6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8eda6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8eda6-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8eda6-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8eda6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8eda6-111">Return value</span></span>

<span data-ttu-id="8eda6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8eda6-112">S_OK</span></span> 
  
> <span data-ttu-id="8eda6-113">Las entradas especificadas se han eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8eda6-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="8eda6-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8eda6-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="8eda6-115">La llamada se ha realizado correctamente, pero no se podrían eliminar uno o más de las entradas.</span><span class="sxs-lookup"><span data-stu-id="8eda6-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="8eda6-116">Cuando se devuelve este valor, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="8eda6-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8eda6-117">Para probar este valor, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="8eda6-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8eda6-118">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8eda6-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="8eda6-119">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8eda6-119">MFCMAPI reference</span></span>

<span data-ttu-id="8eda6-120">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8eda6-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8eda6-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8eda6-121">**File**</span></span>|<span data-ttu-id="8eda6-122">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="8eda6-122">**Function**</span></span>|<span data-ttu-id="8eda6-123">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="8eda6-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8eda6-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8eda6-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="8eda6-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="8eda6-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="8eda6-126">MFCMAPI usa el método **DeleteEntries** para eliminar una entrada específica de un contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8eda6-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8eda6-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="8eda6-127">See also</span></span>



[<span data-ttu-id="8eda6-128">IABContainer: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8eda6-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="8eda6-129">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="8eda6-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

